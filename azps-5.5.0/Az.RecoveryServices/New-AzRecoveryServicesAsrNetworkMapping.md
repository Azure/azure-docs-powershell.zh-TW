---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dca68a4f6315ee124c927d0efb0ff0eb95bf1663
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134702"
---
# <span data-ttu-id="7ca2d-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7ca2d-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="7ca2d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ca2d-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca2d-103">在兩個網路之間建立 ASR 網路對應。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="7ca2d-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ca2d-104">SYNTAX</span></span>

### <span data-ttu-id="7ca2d-105">EnterpriseToEnterprise (預設) </span><span class="sxs-lookup"><span data-stu-id="7ca2d-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ca2d-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="7ca2d-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca2d-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="7ca2d-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ca2d-108">說明</span><span class="sxs-lookup"><span data-stu-id="7ca2d-108">DESCRIPTION</span></span>
<span data-ttu-id="7ca2d-109">**新的-AzRecoveryServicesAsrNetworkMapping** Cmdlet 會啟動在兩個網路之間建立 ASR 網路對應的作業，並傳回用於追蹤作業之 asr 作業的 asr 工作物件。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="7ca2d-110">示例</span><span class="sxs-lookup"><span data-stu-id="7ca2d-110">EXAMPLES</span></span>

### <span data-ttu-id="7ca2d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7ca2d-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="7ca2d-112">使用指定的名稱、主要和恢復網路來啟動網路對應建立作業，並傳回 ASR 作業來追蹤作業。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="7ca2d-113">範例2</span><span class="sxs-lookup"><span data-stu-id="7ca2d-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="7ca2d-114">使用指定的名稱、主要和恢復網路，啟動建立作業的網路對應，然後傳回 ASR 作業，以追蹤 (Azure 到 Azure 案例) 的操作。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="7ca2d-115">參數</span><span class="sxs-lookup"><span data-stu-id="7ca2d-115">PARAMETERS</span></span>

### <span data-ttu-id="7ca2d-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="7ca2d-116">-AzureToAzure</span></span>
<span data-ttu-id="7ca2d-117">[標誌] 來建立 AzureToAzure 案例。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-117">Flag to create AzureToAzure scenario.</span></span>

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

### <span data-ttu-id="7ca2d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca2d-118">-DefaultProfile</span></span>
<span data-ttu-id="7ca2d-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="7ca2d-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="7ca2d-120">-Name</span></span>
<span data-ttu-id="7ca2d-121">要建立之 ASR 網路對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="7ca2d-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="7ca2d-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="7ca2d-123">指定對應之主要網路的 Azure 虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

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

### <span data-ttu-id="7ca2d-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="7ca2d-124">-PrimaryFabric</span></span>
<span data-ttu-id="7ca2d-125">指定應建立對應的 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-125">Specifies the ASR fabric where mapping should be created.</span></span>

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

### <span data-ttu-id="7ca2d-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="7ca2d-126">-PrimaryNetwork</span></span>
<span data-ttu-id="7ca2d-127">指定 ASR 網路對應的主要網路物件。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-127">Specifies the primary network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="7ca2d-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="7ca2d-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="7ca2d-129">指定網路對應的 [恢復 azure 網路識別碼]。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-129">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="7ca2d-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="7ca2d-130">-RecoveryFabric</span></span>
<span data-ttu-id="7ca2d-131">對應到復原 Azure 區域的 Azure Site Recovery fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

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

### <span data-ttu-id="7ca2d-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="7ca2d-132">-RecoveryNetwork</span></span>
<span data-ttu-id="7ca2d-133">指定 ASR 網路對應的恢復網路物件。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-133">Specifies the recovery network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="7ca2d-134">-確認</span><span class="sxs-lookup"><span data-stu-id="7ca2d-134">-Confirm</span></span>
<span data-ttu-id="7ca2d-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ca2d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ca2d-136">-WhatIf</span></span>
<span data-ttu-id="7ca2d-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ca2d-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ca2d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca2d-139">CommonParameters</span></span>
<span data-ttu-id="7ca2d-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca2d-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7ca2d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca2d-142">輸入</span><span class="sxs-lookup"><span data-stu-id="7ca2d-142">INPUTS</span></span>

### <span data-ttu-id="7ca2d-143">RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="7ca2d-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="7ca2d-144">輸出</span><span class="sxs-lookup"><span data-stu-id="7ca2d-144">OUTPUTS</span></span>

### <span data-ttu-id="7ca2d-145">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7ca2d-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7ca2d-146">筆記</span><span class="sxs-lookup"><span data-stu-id="7ca2d-146">NOTES</span></span>

## <span data-ttu-id="7ca2d-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ca2d-147">RELATED LINKS</span></span>

[<span data-ttu-id="7ca2d-148">AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7ca2d-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="7ca2d-149">移除-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="7ca2d-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
