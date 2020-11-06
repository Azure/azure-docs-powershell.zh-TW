---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrFabric.md
ms.openlocfilehash: 8604d1a648590e0fc88a268e6bf2941bbf9344e1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621118"
---
# <span data-ttu-id="ed921-101">New-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ed921-101">New-AzRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="ed921-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed921-102">SYNOPSIS</span></span>
<span data-ttu-id="ed921-103">建立 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="ed921-103">Creates an Azure Site Recovery Fabric.</span></span>

## <span data-ttu-id="ed921-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed921-104">SYNTAX</span></span>

### <span data-ttu-id="ed921-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="ed921-105">Default (Default)</span></span>
```
New-AzRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed921-106">Azure</span><span class="sxs-lookup"><span data-stu-id="ed921-106">Azure</span></span>
```
New-AzRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed921-107">說明</span><span class="sxs-lookup"><span data-stu-id="ed921-107">DESCRIPTION</span></span>
<span data-ttu-id="ed921-108">**新的-AzRecoveryServicesAsrFabric** Cmdlet 會建立指定類型的 Azure Site Recovery 結構。</span><span class="sxs-lookup"><span data-stu-id="ed921-108">The **New-AzRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="ed921-109">示例</span><span class="sxs-lookup"><span data-stu-id="ed921-109">EXAMPLES</span></span>

### <span data-ttu-id="ed921-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ed921-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="ed921-111">使用傳遞的名稱開始建立結構，並傳回用於追蹤結構建立作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="ed921-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="ed921-112">範例2</span><span class="sxs-lookup"><span data-stu-id="ed921-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzRecoveryServicesAsrFabric -Az -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="ed921-113">使用傳遞的名稱開始建立 azure 結構，並傳回用於追蹤結構建立作業的 ASR 作業。</span><span class="sxs-lookup"><span data-stu-id="ed921-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="ed921-114">參數</span><span class="sxs-lookup"><span data-stu-id="ed921-114">PARAMETERS</span></span>

### <span data-ttu-id="ed921-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="ed921-115">-Azure</span></span>
<span data-ttu-id="ed921-116">{{Fill Azure 說明}}</span><span class="sxs-lookup"><span data-stu-id="ed921-116">{{Fill Azure Description}}</span></span>

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

### <span data-ttu-id="ed921-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed921-117">-DefaultProfile</span></span>
<span data-ttu-id="ed921-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed921-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ed921-119">-位置</span><span class="sxs-lookup"><span data-stu-id="ed921-119">-Location</span></span>
<span data-ttu-id="ed921-120">指定對應至所建立結構物件的 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="ed921-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="ed921-121">Azure Site Recovery fabric 物件代表一個區域。</span><span class="sxs-lookup"><span data-stu-id="ed921-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="ed921-122">對於在兩個 Azure 區域之間複製的虛擬機器，主要結構代表主要 Azure 區域和恢復結構。</span><span class="sxs-lookup"><span data-stu-id="ed921-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

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

### <span data-ttu-id="ed921-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="ed921-123">-Name</span></span>
<span data-ttu-id="ed921-124">指定 Azure 網站復原結構的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed921-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="ed921-125">-類型</span><span class="sxs-lookup"><span data-stu-id="ed921-125">-Type</span></span>
<span data-ttu-id="ed921-126">指定 Azure Site Recovery 結構類型。</span><span class="sxs-lookup"><span data-stu-id="ed921-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

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

### <span data-ttu-id="ed921-127">-確認</span><span class="sxs-lookup"><span data-stu-id="ed921-127">-Confirm</span></span>
<span data-ttu-id="ed921-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed921-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed921-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed921-129">-WhatIf</span></span>
<span data-ttu-id="ed921-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed921-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed921-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed921-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed921-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed921-132">CommonParameters</span></span>
<span data-ttu-id="ed921-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed921-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed921-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed921-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed921-135">輸入</span><span class="sxs-lookup"><span data-stu-id="ed921-135">INPUTS</span></span>

### <span data-ttu-id="ed921-136">所有</span><span class="sxs-lookup"><span data-stu-id="ed921-136">None</span></span>

## <span data-ttu-id="ed921-137">輸出</span><span class="sxs-lookup"><span data-stu-id="ed921-137">OUTPUTS</span></span>

### <span data-ttu-id="ed921-138">RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ed921-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ed921-139">筆記</span><span class="sxs-lookup"><span data-stu-id="ed921-139">NOTES</span></span>

## <span data-ttu-id="ed921-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed921-140">RELATED LINKS</span></span>

[<span data-ttu-id="ed921-141">AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ed921-141">Get-AzRecoveryServicesAsrFabric</span></span>](./Get-AzRecoveryServicesAsrFabric.md)

[<span data-ttu-id="ed921-142">移除-AzRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="ed921-142">Remove-AzRecoveryServicesAsrFabric</span></span>](./Remove-AzRecoveryServicesAsrFabric.md)
