---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 1da06582d442c96f74579e9fdf3009325f996012
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625765"
---
# <span data-ttu-id="2eb7c-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="2eb7c-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="2eb7c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2eb7c-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb7c-103">建立 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eb7c-104">句法</span><span class="sxs-lookup"><span data-stu-id="2eb7c-104">SYNTAX</span></span>

### <span data-ttu-id="2eb7c-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="2eb7c-105">Default (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb7c-106">Azure</span><span class="sxs-lookup"><span data-stu-id="2eb7c-106">Azure</span></span>
```
New-AzureRmRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eb7c-107">說明</span><span class="sxs-lookup"><span data-stu-id="2eb7c-107">DESCRIPTION</span></span>
<span data-ttu-id="2eb7c-108">**新的-AzureRmRecoveryServicesAsrFabric** Cmdlet 會建立指定類型的 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-108">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="2eb7c-109">示例</span><span class="sxs-lookup"><span data-stu-id="2eb7c-109">EXAMPLES</span></span>

### <span data-ttu-id="2eb7c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2eb7c-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="2eb7c-111">使用傳遞的名稱開始建立結構，並傳回用於追蹤結構建立作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="2eb7c-112">範例2</span><span class="sxs-lookup"><span data-stu-id="2eb7c-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="2eb7c-113">使用傳遞的名稱開始建立 azure 結構，並傳回用於追蹤結構建立作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="2eb7c-114">參數</span><span class="sxs-lookup"><span data-stu-id="2eb7c-114">PARAMETERS</span></span>

### <span data-ttu-id="2eb7c-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="2eb7c-115">-Azure</span></span>
<span data-ttu-id="2eb7c-116">切換參數表示建立 azure fabric。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-116">Switch parameter indicates creation of azure fabric.</span></span>

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

### <span data-ttu-id="2eb7c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb7c-117">-DefaultProfile</span></span>
<span data-ttu-id="2eb7c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2eb7c-119">-位置</span><span class="sxs-lookup"><span data-stu-id="2eb7c-119">-Location</span></span>
<span data-ttu-id="2eb7c-120">指定對應至所建立結構物件的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="2eb7c-121">Azure Site Recovery fabric 物件代表一個區域。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="2eb7c-122">對於在兩個 Azure 區域之間複製的虛擬機器，主要結構代表主要 Azure 區域和恢復結構。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="2eb7c-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="2eb7c-123">-Name</span></span>
<span data-ttu-id="2eb7c-124">指定 Azure 網站復原結構的名稱。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="2eb7c-125">-類型</span><span class="sxs-lookup"><span data-stu-id="2eb7c-125">-Type</span></span>
<span data-ttu-id="2eb7c-126">指定 Azure Site Recovery 結構類型。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="2eb7c-127">-確認</span><span class="sxs-lookup"><span data-stu-id="2eb7c-127">-Confirm</span></span>
<span data-ttu-id="2eb7c-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eb7c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eb7c-129">-WhatIf</span></span>
<span data-ttu-id="2eb7c-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2eb7c-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eb7c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb7c-132">CommonParameters</span></span>
<span data-ttu-id="2eb7c-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb7c-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2eb7c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb7c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="2eb7c-135">INPUTS</span></span>

### <span data-ttu-id="2eb7c-136">所有</span><span class="sxs-lookup"><span data-stu-id="2eb7c-136">None</span></span>

## <span data-ttu-id="2eb7c-137">輸出</span><span class="sxs-lookup"><span data-stu-id="2eb7c-137">OUTPUTS</span></span>

### <span data-ttu-id="2eb7c-138">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2eb7c-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2eb7c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="2eb7c-139">NOTES</span></span>

## <span data-ttu-id="2eb7c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="2eb7c-140">RELATED LINKS</span></span>

[<span data-ttu-id="2eb7c-141">AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="2eb7c-141">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="2eb7c-142">移除-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="2eb7c-142">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)