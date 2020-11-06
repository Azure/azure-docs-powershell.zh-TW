---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 0cabaee1c1d9dfc8a627160ac01adaca81fe65c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452103"
---
# <span data-ttu-id="db7bb-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="db7bb-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="db7bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db7bb-102">SYNOPSIS</span></span>
<span data-ttu-id="db7bb-103">更新 Azure 網站復原方案的內容。</span><span class="sxs-lookup"><span data-stu-id="db7bb-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db7bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="db7bb-104">SYNTAX</span></span>

### <span data-ttu-id="db7bb-105">ByRPObject (預設) </span><span class="sxs-lookup"><span data-stu-id="db7bb-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db7bb-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="db7bb-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db7bb-107">說明</span><span class="sxs-lookup"><span data-stu-id="db7bb-107">DESCRIPTION</span></span>
<span data-ttu-id="db7bb-108">**AzureRmRecoveryServicesAsrRecoveryPlan** Cmdlet 會使用指定的 ASR 恢復方案物件或 ASR 復原方案定義 json 檔案的內容來更新復原方案的內容。</span><span class="sxs-lookup"><span data-stu-id="db7bb-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="db7bb-109">示例</span><span class="sxs-lookup"><span data-stu-id="db7bb-109">EXAMPLES</span></span>

### <span data-ttu-id="db7bb-110">範例1：更新復原方案</span><span class="sxs-lookup"><span data-stu-id="db7bb-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="db7bb-111">使用指定的 ASR 恢復方案物件的內容來開始更新復原方案，並傳回用來追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="db7bb-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="db7bb-112">參數</span><span class="sxs-lookup"><span data-stu-id="db7bb-112">PARAMETERS</span></span>

### <span data-ttu-id="db7bb-113">-確認</span><span class="sxs-lookup"><span data-stu-id="db7bb-113">-Confirm</span></span>
<span data-ttu-id="db7bb-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="db7bb-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db7bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db7bb-115">-DefaultProfile</span></span>
<span data-ttu-id="db7bb-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="db7bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="db7bb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db7bb-117">-InputObject</span></span>
<span data-ttu-id="db7bb-118">Cmdlet 的輸入物件：指定 ASR 復原方案物件，這些物件的內容是用來更新物件所參照的復原方案。</span><span class="sxs-lookup"><span data-stu-id="db7bb-118">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db7bb-119">-Path</span><span class="sxs-lookup"><span data-stu-id="db7bb-119">-Path</span></span>
<span data-ttu-id="db7bb-120">指定用來更新復原方案之復原方案定義 json 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="db7bb-120">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db7bb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db7bb-121">-WhatIf</span></span>
<span data-ttu-id="db7bb-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="db7bb-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db7bb-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db7bb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db7bb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db7bb-124">CommonParameters</span></span>
<span data-ttu-id="db7bb-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db7bb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db7bb-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="db7bb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db7bb-127">輸入</span><span class="sxs-lookup"><span data-stu-id="db7bb-127">INPUTS</span></span>

### <span data-ttu-id="db7bb-128">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="db7bb-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="db7bb-129">輸出</span><span class="sxs-lookup"><span data-stu-id="db7bb-129">OUTPUTS</span></span>

### <span data-ttu-id="db7bb-130">System.object</span><span class="sxs-lookup"><span data-stu-id="db7bb-130">System.Object</span></span>

## <span data-ttu-id="db7bb-131">筆記</span><span class="sxs-lookup"><span data-stu-id="db7bb-131">NOTES</span></span>

## <span data-ttu-id="db7bb-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="db7bb-132">RELATED LINKS</span></span>

[<span data-ttu-id="db7bb-133">AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="db7bb-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="db7bb-134">新-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="db7bb-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="db7bb-135">移除-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="db7bb-135">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)
