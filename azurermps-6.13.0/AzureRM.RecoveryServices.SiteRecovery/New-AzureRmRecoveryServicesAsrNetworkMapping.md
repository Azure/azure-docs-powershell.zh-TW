---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: e9aadbc8eae9703340043dc640f4cb9759b919d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623404"
---
# <span data-ttu-id="284d2-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="284d2-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="284d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="284d2-102">SYNOPSIS</span></span>
<span data-ttu-id="284d2-103">在兩個網路之間建立 ASR 網路對應。</span><span class="sxs-lookup"><span data-stu-id="284d2-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="284d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="284d2-104">SYNTAX</span></span>

### <span data-ttu-id="284d2-105">EnterpriseToEnterprise (預設) </span><span class="sxs-lookup"><span data-stu-id="284d2-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="284d2-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="284d2-106">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="284d2-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="284d2-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="284d2-108">說明</span><span class="sxs-lookup"><span data-stu-id="284d2-108">DESCRIPTION</span></span>
<span data-ttu-id="284d2-109">**新的-AzureRmRecoveryServicesAsrNetworkMapping** Cmdlet 會啟動在兩個網路之間建立 ASR 網路對應的作業，並傳回用於追蹤作業之 asr 作業的 asr 工作物件。</span><span class="sxs-lookup"><span data-stu-id="284d2-109">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="284d2-110">示例</span><span class="sxs-lookup"><span data-stu-id="284d2-110">EXAMPLES</span></span>

### <span data-ttu-id="284d2-111">範例1</span><span class="sxs-lookup"><span data-stu-id="284d2-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="284d2-112">使用指定的名稱、主要和恢復網路來啟動網路對應建立作業，並傳回 ASR 作業來追蹤作業。</span><span class="sxs-lookup"><span data-stu-id="284d2-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="284d2-113">範例2</span><span class="sxs-lookup"><span data-stu-id="284d2-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="284d2-114">使用指定的名稱、主要和恢復網路，啟動建立作業的網路對應，然後傳回 ASR 作業，以追蹤 (Azure 到 Azure 案例) 的操作。</span><span class="sxs-lookup"><span data-stu-id="284d2-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="284d2-115">參數</span><span class="sxs-lookup"><span data-stu-id="284d2-115">PARAMETERS</span></span>

### <span data-ttu-id="284d2-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="284d2-116">-AzureToAzure</span></span>
<span data-ttu-id="284d2-117">[切換參數]：指定所建立的網路對應將用於在兩個 Azure 區域之間複製 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="284d2-117">Switch parameter specifying that the network mapping being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

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

### <span data-ttu-id="284d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="284d2-118">-DefaultProfile</span></span>
<span data-ttu-id="284d2-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="284d2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="284d2-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="284d2-120">-Name</span></span>
<span data-ttu-id="284d2-121">要建立之 ASR 網路對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="284d2-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="284d2-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="284d2-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="284d2-123">指定對應之主要網路的 Azure 虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="284d2-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

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

### <span data-ttu-id="284d2-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="284d2-124">-PrimaryFabric</span></span>
<span data-ttu-id="284d2-125">Specifes 應建立對應的 ASR 結構。</span><span class="sxs-lookup"><span data-stu-id="284d2-125">Specifes the ASR fabric where mapping should be created.</span></span>

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

### <span data-ttu-id="284d2-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="284d2-126">-PrimaryNetwork</span></span>
<span data-ttu-id="284d2-127">指定 ASR 網路對應的主要網路物件。</span><span class="sxs-lookup"><span data-stu-id="284d2-127">Specifies the primary network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="284d2-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="284d2-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="284d2-129">指定網路對應的 [恢復 azure 網路識別碼]。</span><span class="sxs-lookup"><span data-stu-id="284d2-129">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="284d2-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="284d2-130">-RecoveryFabric</span></span>
<span data-ttu-id="284d2-131">對應到復原 Azure 區域的 Azure Site Recovery fabric 物件。</span><span class="sxs-lookup"><span data-stu-id="284d2-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

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

### <span data-ttu-id="284d2-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="284d2-132">-RecoveryNetwork</span></span>
<span data-ttu-id="284d2-133">指定 ASR 網路對應的恢復網路物件。</span><span class="sxs-lookup"><span data-stu-id="284d2-133">Specifies the recovery network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="284d2-134">-確認</span><span class="sxs-lookup"><span data-stu-id="284d2-134">-Confirm</span></span>
<span data-ttu-id="284d2-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="284d2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="284d2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="284d2-136">-WhatIf</span></span>
<span data-ttu-id="284d2-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="284d2-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="284d2-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="284d2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="284d2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="284d2-139">CommonParameters</span></span>
<span data-ttu-id="284d2-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="284d2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="284d2-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="284d2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="284d2-142">輸入</span><span class="sxs-lookup"><span data-stu-id="284d2-142">INPUTS</span></span>

### <span data-ttu-id="284d2-143">RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="284d2-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="284d2-144">輸出</span><span class="sxs-lookup"><span data-stu-id="284d2-144">OUTPUTS</span></span>

### <span data-ttu-id="284d2-145">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="284d2-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="284d2-146">筆記</span><span class="sxs-lookup"><span data-stu-id="284d2-146">NOTES</span></span>

## <span data-ttu-id="284d2-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="284d2-147">RELATED LINKS</span></span>

[<span data-ttu-id="284d2-148">AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="284d2-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="284d2-149">移除-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="284d2-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
