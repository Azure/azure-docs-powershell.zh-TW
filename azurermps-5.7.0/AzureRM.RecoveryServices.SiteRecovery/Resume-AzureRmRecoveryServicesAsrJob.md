---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/resume-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e6c384f56e7af9bacad40dfbc1fbf87d26dd8320
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448605"
---
# <span data-ttu-id="61e5c-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="61e5c-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="61e5c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="61e5c-103">繼續已暫停的 Azure 網站還原作業。</span><span class="sxs-lookup"><span data-stu-id="61e5c-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61e5c-104">句法</span><span class="sxs-lookup"><span data-stu-id="61e5c-104">SYNTAX</span></span>

### <span data-ttu-id="61e5c-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="61e5c-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61e5c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="61e5c-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61e5c-107">說明</span><span class="sxs-lookup"><span data-stu-id="61e5c-107">DESCRIPTION</span></span>
<span data-ttu-id="61e5c-108">**Resume AzureRmRecoveryServicesAsrJob** Cmdlet 會繼續執行暫停的 Azure 網站還原作業。</span><span class="sxs-lookup"><span data-stu-id="61e5c-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="61e5c-109">示例</span><span class="sxs-lookup"><span data-stu-id="61e5c-109">EXAMPLES</span></span>

### <span data-ttu-id="61e5c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="61e5c-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="61e5c-111">如果指定的工作處於 [等待] 或 [暫停] 狀態，並傳回對應至 ASR 作業的更新 ASR 工作物件，請繼續執行該作業。</span><span class="sxs-lookup"><span data-stu-id="61e5c-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="61e5c-112">參數</span><span class="sxs-lookup"><span data-stu-id="61e5c-112">PARAMETERS</span></span>

### <span data-ttu-id="61e5c-113">-批註</span><span class="sxs-lookup"><span data-stu-id="61e5c-113">-Comment</span></span>
<span data-ttu-id="61e5c-114">作業記錄的批註。</span><span class="sxs-lookup"><span data-stu-id="61e5c-114">Comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e5c-115">-確認</span><span class="sxs-lookup"><span data-stu-id="61e5c-115">-Confirm</span></span>
<span data-ttu-id="61e5c-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61e5c-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e5c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e5c-117">-DefaultProfile</span></span>
<span data-ttu-id="61e5c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61e5c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="61e5c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61e5c-119">-InputObject</span></span>
<span data-ttu-id="61e5c-120">Cmdlet 的輸入物件：對應至要繼續作業的 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="61e5c-120">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61e5c-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="61e5c-121">-Name</span></span>
<span data-ttu-id="61e5c-122">依名稱指定 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="61e5c-122">Specify the ASR job by name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e5c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61e5c-123">-WhatIf</span></span>
<span data-ttu-id="61e5c-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61e5c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61e5c-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61e5c-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61e5c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e5c-126">CommonParameters</span></span>
<span data-ttu-id="61e5c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61e5c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e5c-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61e5c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e5c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="61e5c-129">INPUTS</span></span>

### <span data-ttu-id="61e5c-130">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="61e5c-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="61e5c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="61e5c-131">OUTPUTS</span></span>

### <span data-ttu-id="61e5c-132">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="61e5c-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="61e5c-133">筆記</span><span class="sxs-lookup"><span data-stu-id="61e5c-133">NOTES</span></span>

## <span data-ttu-id="61e5c-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="61e5c-134">RELATED LINKS</span></span>

[<span data-ttu-id="61e5c-135">AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="61e5c-135">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="61e5c-136">重新開機-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="61e5c-136">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="61e5c-137">停止 AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="61e5c-137">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
