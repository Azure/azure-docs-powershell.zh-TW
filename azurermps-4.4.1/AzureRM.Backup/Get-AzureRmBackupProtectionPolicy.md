---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: B3B708C5-776E-4F1C-BA0B-492CD9057794
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 08cfb4279199455b14794a890b398fd954cb4cd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447168"
---
# <span data-ttu-id="9dbd2-101">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9dbd2-101">Get-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="9dbd2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9dbd2-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbd2-103">取得備份保存庫的備份原則。</span><span class="sxs-lookup"><span data-stu-id="9dbd2-103">Gets backup policies for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9dbd2-104">句法</span><span class="sxs-lookup"><span data-stu-id="9dbd2-104">SYNTAX</span></span>

```
Get-AzureRmBackupProtectionPolicy [[-Name] <String>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dbd2-105">說明</span><span class="sxs-lookup"><span data-stu-id="9dbd2-105">DESCRIPTION</span></span>
<span data-ttu-id="9dbd2-106">**AzureRmBackupProtectionPolicy** Cmdlet 會取得 Azure 備份電子倉庫的備份原則。</span><span class="sxs-lookup"><span data-stu-id="9dbd2-106">The **Get-AzureRmBackupProtectionPolicy** cmdlet gets backup policies for an Azure Backup vault.</span></span>

## <span data-ttu-id="9dbd2-107">示例</span><span class="sxs-lookup"><span data-stu-id="9dbd2-107">EXAMPLES</span></span>

### <span data-ttu-id="9dbd2-108">範例1：在電子倉庫中查看原則</span><span class="sxs-lookup"><span data-stu-id="9dbd2-108">Example 1: View the policies in a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault 
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
contoso01                 AzureVM            Daily              26-Aug-15 3:00:00 PM
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
WeeklyBkp                 AzureVM            Weekly             26-Aug-15 5:00:00 PM
contoso02                 AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="9dbd2-109">第一個命令會使用 **AzureRmBackupVault** Cmdlet 取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="9dbd2-109">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="9dbd2-110">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="9dbd2-110">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="9dbd2-111">第二個命令會在 $Vault 中取得電子倉庫的所有備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="9dbd2-111">The second command gets all the Backup protection policies for the vault in $Vault.</span></span>

### <span data-ttu-id="9dbd2-112">範例2：從電子倉庫取得特定原則</span><span class="sxs-lookup"><span data-stu-id="9dbd2-112">Example 2: Get a specific policy from a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
```

<span data-ttu-id="9dbd2-113">第一個命令會使用 **AzureRmBackupVault** Cmdlet 取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="9dbd2-113">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="9dbd2-114">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="9dbd2-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="9dbd2-115">第二個命令會針對 $Vault 中的電子倉庫，取得名為 DefaultPolicy 的備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="9dbd2-115">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>

## <span data-ttu-id="9dbd2-116">參數</span><span class="sxs-lookup"><span data-stu-id="9dbd2-116">PARAMETERS</span></span>

### <span data-ttu-id="9dbd2-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="9dbd2-117">-Name</span></span>
<span data-ttu-id="9dbd2-118">指定此 Cmdlet 所取得原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9dbd2-118">Specifies the name of the policy that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dbd2-119">-保存庫</span><span class="sxs-lookup"><span data-stu-id="9dbd2-119">-Vault</span></span>
<span data-ttu-id="9dbd2-120">指定此 Cmdlet 取得其原則的備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="9dbd2-120">Specifies the Backup vault for which this cmdlet gets policies.</span></span>
<span data-ttu-id="9dbd2-121">若要取得 **AzureRmBackupVault** 物件，請使用 Get-AzureRmBackupVault Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9dbd2-121">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9dbd2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dbd2-122">-DefaultProfile</span></span>
<span data-ttu-id="9dbd2-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9dbd2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9dbd2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbd2-124">CommonParameters</span></span>
<span data-ttu-id="9dbd2-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9dbd2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbd2-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9dbd2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbd2-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9dbd2-127">INPUTS</span></span>

### <span data-ttu-id="9dbd2-128">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9dbd2-128">AzureRmBackupVault</span></span>

## <span data-ttu-id="9dbd2-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9dbd2-129">OUTPUTS</span></span>

### <span data-ttu-id="9dbd2-130">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9dbd2-130">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="9dbd2-131">筆記</span><span class="sxs-lookup"><span data-stu-id="9dbd2-131">NOTES</span></span>
* <span data-ttu-id="9dbd2-132">所有</span><span class="sxs-lookup"><span data-stu-id="9dbd2-132">None</span></span>

## <span data-ttu-id="9dbd2-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="9dbd2-133">RELATED LINKS</span></span>

[<span data-ttu-id="9dbd2-134">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="9dbd2-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="9dbd2-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9dbd2-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="9dbd2-136">新-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9dbd2-136">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="9dbd2-137">移除-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9dbd2-137">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)


