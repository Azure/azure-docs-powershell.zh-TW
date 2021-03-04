---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: bfea43fb0f27aff6405159c0174a698d9dc2298e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915238"
---
# <span data-ttu-id="c2843-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="c2843-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="c2843-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c2843-102">SYNOPSIS</span></span>
<span data-ttu-id="c2843-103">建立 Azure 網站修復結構。</span><span class="sxs-lookup"><span data-stu-id="c2843-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="c2843-104">語法</span><span class="sxs-lookup"><span data-stu-id="c2843-104">SYNTAX</span></span>

### <span data-ttu-id="c2843-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="c2843-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2843-106">蔚藍</span><span class="sxs-lookup"><span data-stu-id="c2843-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2843-107">描述</span><span class="sxs-lookup"><span data-stu-id="c2843-107">DESCRIPTION</span></span>
<span data-ttu-id="c2843-108">**New-AzRecoveryServicesAsrFabric** Cmdlet 會建立指定類型的 Azure 網站修復結構。</span><span class="sxs-lookup"><span data-stu-id="c2843-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="c2843-109">例子</span><span class="sxs-lookup"><span data-stu-id="c2843-109">EXAMPLES</span></span>

### <span data-ttu-id="c2843-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="c2843-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="c2843-111">以傳遞的名稱開始建立布料，並傳回用來追蹤布料建立作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="c2843-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="c2843-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="c2843-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="c2843-113">以傳遞的名稱開始建立 Azure 結構，並傳回用來追蹤布料建立作業的 ASR 工作。</span><span class="sxs-lookup"><span data-stu-id="c2843-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="c2843-114">參數</span><span class="sxs-lookup"><span data-stu-id="c2843-114">PARAMETERS</span></span>

### <span data-ttu-id="c2843-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="c2843-115">-Azure</span></span>
<span data-ttu-id="c2843-116">Switch 參數指定建立 Azure 結構。</span><span class="sxs-lookup"><span data-stu-id="c2843-116">Switch parameter specifies to create azure fabric.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2843-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2843-117">-DefaultProfile</span></span>
<span data-ttu-id="c2843-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c2843-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2843-119">-位置</span><span class="sxs-lookup"><span data-stu-id="c2843-119">-Location</span></span>
<span data-ttu-id="c2843-120">指定與要建立之結構物件對應的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="c2843-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="c2843-121">Azure 網站復原結構物件代表區域。</span><span class="sxs-lookup"><span data-stu-id="c2843-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="c2843-122">針對在兩個 Azure 區域之間複製的虛擬機器，主要結構代表主要的 Azure 區域及復原結構。</span><span class="sxs-lookup"><span data-stu-id="c2843-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: System.String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2843-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c2843-123">-Name</span></span>
<span data-ttu-id="c2843-124">指定 Azure 網站修復結構的名稱。</span><span class="sxs-lookup"><span data-stu-id="c2843-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2843-125">-類型</span><span class="sxs-lookup"><span data-stu-id="c2843-125">-Type</span></span>
<span data-ttu-id="c2843-126">指定 Azure 網站修復結構類型。</span><span class="sxs-lookup"><span data-stu-id="c2843-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2843-127">-確認</span><span class="sxs-lookup"><span data-stu-id="c2843-127">-Confirm</span></span>
<span data-ttu-id="c2843-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c2843-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2843-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2843-129">-WhatIf</span></span>
<span data-ttu-id="c2843-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c2843-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2843-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c2843-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2843-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2843-132">CommonParameters</span></span>
<span data-ttu-id="c2843-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c2843-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2843-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2843-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2843-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c2843-135">INPUTS</span></span>

### <span data-ttu-id="c2843-136">沒有</span><span class="sxs-lookup"><span data-stu-id="c2843-136">None</span></span>

## <span data-ttu-id="c2843-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c2843-137">OUTPUTS</span></span>

### <span data-ttu-id="c2843-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="c2843-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c2843-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c2843-139">NOTES</span></span>

## <span data-ttu-id="c2843-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="c2843-140">RELATED LINKS</span></span>

[<span data-ttu-id="c2843-141">Get-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="c2843-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="c2843-142">Remove-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="c2843-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
