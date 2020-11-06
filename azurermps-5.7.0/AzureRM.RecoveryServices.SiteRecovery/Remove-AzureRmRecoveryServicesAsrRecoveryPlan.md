---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 5f4298c2a4bfdc081447e6a8b15bac565b20b2db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448617"
---
# <span data-ttu-id="1d607-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1d607-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="1d607-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d607-102">SYNOPSIS</span></span>
<span data-ttu-id="1d607-103">從 [恢復服務] 保存庫刪除指定的 ASR 恢復方案。</span><span class="sxs-lookup"><span data-stu-id="1d607-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d607-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d607-104">SYNTAX</span></span>

### <span data-ttu-id="1d607-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="1d607-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d607-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1d607-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d607-107">說明</span><span class="sxs-lookup"><span data-stu-id="1d607-107">DESCRIPTION</span></span>
<span data-ttu-id="1d607-108">**AzureRmRecoveryServicesAsrRecoveryPlan** Cmdlet 會從 [恢復服務] 保存庫中刪除指定的復原方案。</span><span class="sxs-lookup"><span data-stu-id="1d607-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="1d607-109">示例</span><span class="sxs-lookup"><span data-stu-id="1d607-109">EXAMPLES</span></span>

### <span data-ttu-id="1d607-110">範例1</span><span class="sxs-lookup"><span data-stu-id="1d607-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="1d607-111">開始刪除指定的復原方案，並傳回用於追蹤作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="1d607-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1d607-112">參數</span><span class="sxs-lookup"><span data-stu-id="1d607-112">PARAMETERS</span></span>

### <span data-ttu-id="1d607-113">-確認</span><span class="sxs-lookup"><span data-stu-id="1d607-113">-Confirm</span></span>
<span data-ttu-id="1d607-114">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1d607-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d607-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d607-115">-DefaultProfile</span></span>
<span data-ttu-id="1d607-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d607-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="1d607-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d607-117">-InputObject</span></span>
<span data-ttu-id="1d607-118">Cmdlet 的輸入物件：對應至要刪除之復原方案的 ASR 恢復方案物件。</span><span class="sxs-lookup"><span data-stu-id="1d607-118">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d607-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="1d607-119">-Name</span></span>
<span data-ttu-id="1d607-120">指定要刪除的復原方案名稱。</span><span class="sxs-lookup"><span data-stu-id="1d607-120">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="1d607-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d607-121">-WhatIf</span></span>
<span data-ttu-id="1d607-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1d607-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1d607-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d607-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d607-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d607-124">CommonParameters</span></span>
<span data-ttu-id="1d607-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d607-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d607-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1d607-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d607-127">輸入</span><span class="sxs-lookup"><span data-stu-id="1d607-127">INPUTS</span></span>

### <span data-ttu-id="1d607-128">RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1d607-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="1d607-129">輸出</span><span class="sxs-lookup"><span data-stu-id="1d607-129">OUTPUTS</span></span>

### <span data-ttu-id="1d607-130">System.object</span><span class="sxs-lookup"><span data-stu-id="1d607-130">System.Object</span></span>

## <span data-ttu-id="1d607-131">筆記</span><span class="sxs-lookup"><span data-stu-id="1d607-131">NOTES</span></span>

## <span data-ttu-id="1d607-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d607-132">RELATED LINKS</span></span>

[<span data-ttu-id="1d607-133">AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1d607-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1d607-134">新-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1d607-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1d607-135">更新-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1d607-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


