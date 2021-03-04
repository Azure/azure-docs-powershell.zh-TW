---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: f06635819979823bbbdd298d3873c45ac0a5621a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909498"
---
# <span data-ttu-id="3a3f3-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3a3f3-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="3a3f3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3a3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="3a3f3-103">在兩個網路之間建立 ASR 網路映射。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="3a3f3-104">語法</span><span class="sxs-lookup"><span data-stu-id="3a3f3-104">SYNTAX</span></span>

### <span data-ttu-id="3a3f3-105">EnterpriseToEnterprise (預設) </span><span class="sxs-lookup"><span data-stu-id="3a3f3-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a3f3-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="3a3f3-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a3f3-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="3a3f3-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a3f3-108">描述</span><span class="sxs-lookup"><span data-stu-id="3a3f3-108">DESCRIPTION</span></span>
<span data-ttu-id="3a3f3-109">**New-AzRecoveryServicesAsrNetworkMapping** Cmdlet 會啟動在兩個網路之間建立 ASR 網路地圖的作業，並針對用來追蹤作業的 ASR 工作返回 ASR 工作物件。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="3a3f3-110">例子</span><span class="sxs-lookup"><span data-stu-id="3a3f3-110">EXAMPLES</span></span>

### <span data-ttu-id="3a3f3-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="3a3f3-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="3a3f3-112">使用指定的名稱、主要及復原網路啟動網路地圖建立作業，並返回 ASR 工作來追蹤作業。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="3a3f3-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="3a3f3-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="3a3f3-114">使用指定的名稱、主要及復原網路啟動建立作業的網路地圖，並返回 ASR 工作來追蹤作業 (Azure 到 Azure 案例) 。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="3a3f3-115">參數</span><span class="sxs-lookup"><span data-stu-id="3a3f3-115">PARAMETERS</span></span>

### <span data-ttu-id="3a3f3-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="3a3f3-116">-AzureToAzure</span></span>
<span data-ttu-id="3a3f3-117">標出以建立 AzureToAzure 案例。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-117">Flag to create AzureToAzure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a3f3-118">-DefaultProfile</span></span>
<span data-ttu-id="3a3f3-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3a3f3-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a3f3-120">-Name</span></span>
<span data-ttu-id="3a3f3-121">要建立之 ASR 網路映射的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="3a3f3-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="3a3f3-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="3a3f3-123">指定用於進行地圖的主要網路的 Azure 虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f3-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="3a3f3-124">-PrimaryFabric</span></span>
<span data-ttu-id="3a3f3-125">指定應建立地圖的 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-125">Specifies the ASR fabric where mapping should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f3-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="3a3f3-126">-PrimaryNetwork</span></span>
<span data-ttu-id="3a3f3-127">指定 ASR 網路地圖的主要網路物件。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-127">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f3-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="3a3f3-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="3a3f3-129">指定網路地圖的復原 Azure 網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-129">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f3-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="3a3f3-130">-RecoveryFabric</span></span>
<span data-ttu-id="3a3f3-131">對應到復原 Azure 地區的 Azure 網站修復結構物件。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f3-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="3a3f3-132">-RecoveryNetwork</span></span>
<span data-ttu-id="3a3f3-133">指定 ASR 網路地圖的復原網路物件。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-133">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3f3-134">-確認</span><span class="sxs-lookup"><span data-stu-id="3a3f3-134">-Confirm</span></span>
<span data-ttu-id="3a3f3-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a3f3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a3f3-136">-WhatIf</span></span>
<span data-ttu-id="3a3f3-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a3f3-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a3f3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a3f3-139">CommonParameters</span></span>
<span data-ttu-id="3a3f3-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3a3f3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a3f3-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a3f3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a3f3-142">輸入</span><span class="sxs-lookup"><span data-stu-id="3a3f3-142">INPUTS</span></span>

### <span data-ttu-id="3a3f3-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="3a3f3-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="3a3f3-144">輸出</span><span class="sxs-lookup"><span data-stu-id="3a3f3-144">OUTPUTS</span></span>

### <span data-ttu-id="3a3f3-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="3a3f3-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="3a3f3-146">筆記</span><span class="sxs-lookup"><span data-stu-id="3a3f3-146">NOTES</span></span>

## <span data-ttu-id="3a3f3-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a3f3-147">RELATED LINKS</span></span>

[<span data-ttu-id="3a3f3-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3a3f3-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="3a3f3-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3a3f3-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
