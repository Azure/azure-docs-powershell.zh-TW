---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/stop-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: d219f49bd3fa4660048bdf5108ca660344e2bc48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457463"
---
# <span data-ttu-id="c2597-101">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="c2597-101">Stop-AzureRmBackupJob</span></span>

## <span data-ttu-id="c2597-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c2597-102">SYNOPSIS</span></span>
<span data-ttu-id="c2597-103">取消現有的備份作業。</span><span class="sxs-lookup"><span data-stu-id="c2597-103">Cancels an existing Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2597-104">句法</span><span class="sxs-lookup"><span data-stu-id="c2597-104">SYNTAX</span></span>

### <span data-ttu-id="c2597-105">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="c2597-105">IdFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2597-106">JobFiltersSet</span><span class="sxs-lookup"><span data-stu-id="c2597-106">JobFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2597-107">說明</span><span class="sxs-lookup"><span data-stu-id="c2597-107">DESCRIPTION</span></span>
<span data-ttu-id="c2597-108">**AzureRmBackupJob** Cmdlet 會取消現有的 Azure 備份作業。</span><span class="sxs-lookup"><span data-stu-id="c2597-108">The **Stop-AzureRmBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="c2597-109">使用此參數可停止耗時太長的工作，並封鎖其他活動。</span><span class="sxs-lookup"><span data-stu-id="c2597-109">Use this parameter to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="c2597-110">您只能取消下列作業類型：</span><span class="sxs-lookup"><span data-stu-id="c2597-110">You can cancel only the following types of jobs:</span></span> 

- <span data-ttu-id="c2597-111">備份</span><span class="sxs-lookup"><span data-stu-id="c2597-111">Backup</span></span>
- <span data-ttu-id="c2597-112">還原</span><span class="sxs-lookup"><span data-stu-id="c2597-112">Restore</span></span>

## <span data-ttu-id="c2597-113">示例</span><span class="sxs-lookup"><span data-stu-id="c2597-113">EXAMPLES</span></span>

### <span data-ttu-id="c2597-114">範例1：使用作業 ID 停止備份作業</span><span class="sxs-lookup"><span data-stu-id="c2597-114">Example 1: Stop a backup job by using a job ID</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

<span data-ttu-id="c2597-115">第一個命令會使用 **AzureRmBackupVault** Cmdlet 取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="c2597-115">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="c2597-116">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="c2597-116">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="c2597-117">第二個命令會在 $Vault 中使用 **AzureRmBackupJob** Cmdlet，從 vault 中取得備份作業。</span><span class="sxs-lookup"><span data-stu-id="c2597-117">The second command gets a backup job from the vault in $Vault by using the **Get-AzureRmBackupJob** cmdlet.</span></span>
<span data-ttu-id="c2597-118">該命令會將作業儲存在 $Job 變數中。</span><span class="sxs-lookup"><span data-stu-id="c2597-118">The command stores the job in the $Job variable.</span></span>
<span data-ttu-id="c2597-119">在這個範例中，指定的電子倉庫只有一個備份操作。</span><span class="sxs-lookup"><span data-stu-id="c2597-119">In this example, there is only one backup operation in the specified vault.</span></span>

<span data-ttu-id="c2597-120">最後一個命令會停止具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="c2597-120">The final command stops the job that has the specified ID.</span></span>

### <span data-ttu-id="c2597-121">範例2：停止所有還原作業</span><span class="sxs-lookup"><span data-stu-id="c2597-121">Example 2: Stop all Restore operations</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

<span data-ttu-id="c2597-122">這個命令會在 $Vault 中取得電子倉庫中的所有還原作業，然後使用管線運算子將它們傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2597-122">This command gets all the restore operations in the vault in $Vault, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c2597-123">目前的 Cmdlet 會停止每個作業。</span><span class="sxs-lookup"><span data-stu-id="c2597-123">The current cmdlet stops each job.</span></span>

## <span data-ttu-id="c2597-124">參數</span><span class="sxs-lookup"><span data-stu-id="c2597-124">PARAMETERS</span></span>

### <span data-ttu-id="c2597-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2597-125">-DefaultProfile</span></span>
<span data-ttu-id="c2597-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c2597-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2597-127">-工作</span><span class="sxs-lookup"><span data-stu-id="c2597-127">-Job</span></span>
<span data-ttu-id="c2597-128">指定此 Cmdlet 取消的作業。</span><span class="sxs-lookup"><span data-stu-id="c2597-128">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="c2597-129">若要取得 **AzureRmBackupJob** 物件，請使用 Get-AzureRmBackupJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2597-129">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2597-130">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="c2597-130">-JobID</span></span>
<span data-ttu-id="c2597-131">指定此 Cmdlet 取消的作業。</span><span class="sxs-lookup"><span data-stu-id="c2597-131">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="c2597-132">若要取得 **AzureRmBackupJob** 物件，請使用 Get-AzureRmBackupJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2597-132">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2597-133">-保存庫</span><span class="sxs-lookup"><span data-stu-id="c2597-133">-Vault</span></span>
<span data-ttu-id="c2597-134">指定此 Cmdlet 在其中取消作業的備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="c2597-134">Specifies the Backup vault in which this cmdlet cancels a job.</span></span>
<span data-ttu-id="c2597-135">若要取得 **AzureRmBackupVault** 物件，請使用 Get-AzureRmBackupVault Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2597-135">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2597-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2597-136">CommonParameters</span></span>
<span data-ttu-id="c2597-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c2597-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2597-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c2597-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2597-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c2597-139">INPUTS</span></span>

### <span data-ttu-id="c2597-140">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="c2597-140">AzureRmBackupJob</span></span>

## <span data-ttu-id="c2597-141">輸出</span><span class="sxs-lookup"><span data-stu-id="c2597-141">OUTPUTS</span></span>

### <span data-ttu-id="c2597-142">所有</span><span class="sxs-lookup"><span data-stu-id="c2597-142">None</span></span>

## <span data-ttu-id="c2597-143">筆記</span><span class="sxs-lookup"><span data-stu-id="c2597-143">NOTES</span></span>

## <span data-ttu-id="c2597-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2597-144">RELATED LINKS</span></span>

[<span data-ttu-id="c2597-145">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="c2597-145">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="c2597-146">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="c2597-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="c2597-147">稍候-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="c2597-147">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


