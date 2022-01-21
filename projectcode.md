using MGFinanceApp.IRepository;
using MGFinanceApp.Models;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Threading.Tasks;

namespace MGFinanceApp.Repository
{
    public class BankAccRepository : IBankAccRepository
    {

        private readonly ProjectAddaContext _db;
        public BankAccRepository(ProjectAddaContext db)
        {
            _db = db;

        }
        public BankAcc Add(BankAcc bankAcc)
        {
            bankAcc.UserId = _db.BankAcc.Max(e => e.UserId) + 1;
            _db.BankAcc.Add(bankAcc);
            return bankAcc;
        }

        public BankAcc Delete(int Id)
        {
            BankAcc bankAcc = _db.BankAcc.FirstOrDefault(e => e.UserId == Id);
            if(bankAcc != null)
            {
                _db.BankAcc.Remove(bankAcc);
            }
            return bankAcc;
        }

        public IEnumerable<BankAcc> GetAllBankAcc()
        {
            return _db.BankAcc;
        }

        public BankAcc GetBankAcc(int Id)
        {
            return _db.BankAcc.FirstOrDefault(e => e.UserId == Id);
        }

        public BankAcc Update(BankAcc bankAccChange)
        {
            BankAcc bankAcc = _db.BankAcc.FirstOrDefault(e => e.UserId == bankAccChange.UserId);
            if (bankAcc != null)
            {
                bankAcc.BankName = bankAccChange.BankName;
                bankAcc.Branch = bankAccChange.Branch;
                bankAcc.PaymentEmis = bankAccChange.PaymentEmis;
                
            }
            return bankAcc;
        }
    }
}
