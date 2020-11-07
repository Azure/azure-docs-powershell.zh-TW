---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: bf4ba77a7162faaf593e11b68a82fe5a6e55df1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623936"
---
# <span data-ttu-id="c21dd-101">Get-AzureRmBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="c21dd-101">Get-AzureRmBackupJobDetails</span></span>

## <span data-ttu-id="c21dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c21dd-102">SYNOPSIS</span></span>
<span data-ttu-id="c21dd-103">取得備份作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c21dd-103">Gets the details of a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c21dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="c21dd-104">SYNTAX</span></span>

### <span data-ttu-id="c21dd-105">JobsFiltersSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c21dd-105">JobsFiltersSet (Default)</span></span>
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c21dd-106">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="c21dd-106">IdFiltersSet</span></span>
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c21dd-107">說明</span><span class="sxs-lookup"><span data-stu-id="c21dd-107">DESCRIPTION</span></span>
<span data-ttu-id="c21dd-108">**AzureRmBackupJobDetails** Cmdlet 會取得 Azure 備份作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c21dd-108">The **Get-AzureRmBackupJobDetails** cmdlet gets the details of an Azure Backup job.</span></span>
<span data-ttu-id="c21dd-109">您可以使用這個 Cmdlet 來收集失敗作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c21dd-109">You can use this cmdlet to gather information about a job that fails.</span></span>

## <span data-ttu-id="c21dd-110">示例</span><span class="sxs-lookup"><span data-stu-id="c21dd-110">EXAMPLES</span></span>

### <span data-ttu-id="c21dd-111">範例1：顯示失敗作業的詳細資料</span><span class="sxs-lookup"><span data-stu-id="c21dd-111">Example 1: Display the details of a failed job</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

<span data-ttu-id="c21dd-112">第一個命令會使用 **AzureRmBackupVault** Cmdlet 取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="c21dd-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="c21dd-113">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="c21dd-113">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="c21dd-114">第二個命令會從 $Vault 中的 vault 取得失敗的作業，然後將它們儲存在 $Jobs 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="c21dd-114">The second command gets failed jobs from the vault in $Vault, and then stores them in the $Jobs array variable.</span></span>
<span data-ttu-id="c21dd-115">第三個作業會取得 $Jobs 變數中第一個工作的詳細資料，然後將這些詳細資料儲存在 $JobDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="c21dd-115">The third job gets details for the first job in the $Jobs variable, and then stores those details in the $JobDetails variable.</span></span>
<span data-ttu-id="c21dd-116">Final 命令會使用標準的點語法來顯示 $JobDetails 的 **ErrorDetails** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c21dd-116">The final command displays the **ErrorDetails** property of $JobDetails by using standard dot syntax.</span></span>

### <span data-ttu-id="c21dd-117">範例2：針對失敗的工作顯示建議的動作</span><span class="sxs-lookup"><span data-stu-id="c21dd-117">Example 2: Display the recommended action for a failed job</span></span>
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

<span data-ttu-id="c21dd-118">這個命令會顯示第一個範例中建立的 $JobDetails 變數所建議的動作。</span><span class="sxs-lookup"><span data-stu-id="c21dd-118">This command displays the recommended action from the $JobDetails variable that was created in the first example.</span></span>

## <span data-ttu-id="c21dd-119">參數</span><span class="sxs-lookup"><span data-stu-id="c21dd-119">PARAMETERS</span></span>

### <span data-ttu-id="c21dd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c21dd-120">-DefaultProfile</span></span>
<span data-ttu-id="c21dd-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c21dd-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c21dd-122">-工作</span><span class="sxs-lookup"><span data-stu-id="c21dd-122">-Job</span></span>
<span data-ttu-id="c21dd-123">指定此 Cmdlet 取得詳細資料的作業。</span><span class="sxs-lookup"><span data-stu-id="c21dd-123">Specifies a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="c21dd-124">若要取得 **AzureRmBackupJob** 物件，請使用 Get-AzureRmBackupJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c21dd-124">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c21dd-125">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="c21dd-125">-JobId</span></span>
<span data-ttu-id="c21dd-126">指定此 Cmdlet 所取得之詳細資料的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="c21dd-126">Specifies the ID of a job for which this cmdlet gets details.</span></span>
<span data-ttu-id="c21dd-127">識別碼是 **AzureRmBackupJob** 物件的 **InstanceId** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c21dd-127">The ID is the **InstanceId** property of an **AzureRmBackupJob** object.</span></span>
<span data-ttu-id="c21dd-128">若要取得 **AzureRmBackupJob** 物件，請使用 AzureRmBackupJob。</span><span class="sxs-lookup"><span data-stu-id="c21dd-128">To obtain an **AzureRmBackupJob** object, use Get-AzureRmBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c21dd-129">-保存庫</span><span class="sxs-lookup"><span data-stu-id="c21dd-129">-Vault</span></span>
<span data-ttu-id="c21dd-130">指定此 Cmdlet 取得作業詳細資料的備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="c21dd-130">Specifies the Backup vault for which this cmdlet gets job details.</span></span>
<span data-ttu-id="c21dd-131">若要取得 **AzureRmBackupVault** 物件，請使用 Get-AzureRmBackupVault Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c21dd-131">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c21dd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c21dd-132">CommonParameters</span></span>
<span data-ttu-id="c21dd-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c21dd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c21dd-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c21dd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c21dd-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c21dd-135">INPUTS</span></span>

### <span data-ttu-id="c21dd-136">AzureRMBackupJob 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="c21dd-136">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>
<span data-ttu-id="c21dd-137">參數：作業 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c21dd-137">Parameters: Job (ByValue)</span></span>

## <span data-ttu-id="c21dd-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c21dd-138">OUTPUTS</span></span>

### <span data-ttu-id="c21dd-139">AzureRMBackupJobDetails 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="c21dd-139">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJobDetails</span></span>

## <span data-ttu-id="c21dd-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c21dd-140">NOTES</span></span>

## <span data-ttu-id="c21dd-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="c21dd-141">RELATED LINKS</span></span>

[<span data-ttu-id="c21dd-142">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="c21dd-142">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="c21dd-143">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="c21dd-143">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


