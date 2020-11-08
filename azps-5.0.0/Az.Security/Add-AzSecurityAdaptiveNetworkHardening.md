---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: daccafa4d0100d333d2e686e8b03bb21d8a38736
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139630"
---
# <span data-ttu-id="6492c-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="6492c-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="6492c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6492c-102">SYNOPSIS</span></span>
<span data-ttu-id="6492c-103">在 NSG 中強制執行給定規則 (s) 在要求中列出</span><span class="sxs-lookup"><span data-stu-id="6492c-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="6492c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6492c-104">SYNTAX</span></span>

### <span data-ttu-id="6492c-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="6492c-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6492c-106">說明</span><span class="sxs-lookup"><span data-stu-id="6492c-106">DESCRIPTION</span></span>
<span data-ttu-id="6492c-107">[自我調整網路 Hardenings] 是由 Azure 安全中心自動計算，使用此 Cmdlet 強制執行要求中所列)  (上的指定規則。</span><span class="sxs-lookup"><span data-stu-id="6492c-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="6492c-108">示例</span><span class="sxs-lookup"><span data-stu-id="6492c-108">EXAMPLES</span></span>

### <span data-ttu-id="6492c-109">範例1</span><span class="sxs-lookup"><span data-stu-id="6492c-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="6492c-110">在 NSG 中強制執行給定規則 (s) 在要求中列出</span><span class="sxs-lookup"><span data-stu-id="6492c-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="6492c-111">參數</span><span class="sxs-lookup"><span data-stu-id="6492c-111">PARAMETERS</span></span>

### <span data-ttu-id="6492c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6492c-112">-DefaultProfile</span></span>
<span data-ttu-id="6492c-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6492c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6492c-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="6492c-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="6492c-115">適應網路加強資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="6492c-115">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6492c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6492c-116">-ResourceGroupName</span></span>
<span data-ttu-id="6492c-117">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="6492c-117">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6492c-118">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="6492c-118">-ResourceName</span></span>
<span data-ttu-id="6492c-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="6492c-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6492c-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="6492c-120">-ResourceNamespace</span></span>
<span data-ttu-id="6492c-121">資源的命名空間。</span><span class="sxs-lookup"><span data-stu-id="6492c-121">The Namespace of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNamespace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6492c-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6492c-122">-ResourceType</span></span>
<span data-ttu-id="6492c-123">資源的類型。</span><span class="sxs-lookup"><span data-stu-id="6492c-123">The type of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6492c-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6492c-124">-SubscriptionId</span></span>
<span data-ttu-id="6492c-125">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="6492c-125">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6492c-126">-規則</span><span class="sxs-lookup"><span data-stu-id="6492c-126">-Rules</span></span>
<span data-ttu-id="6492c-127">要強制執行的規則。</span><span class="sxs-lookup"><span data-stu-id="6492c-127">The rules to enforce.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule
Parameter Sets: Rules
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6492c-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="6492c-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="6492c-129">將使用已建立的安全性規則（來自自我調整網路強化規則）來更新之有效網路安全性群組的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6492c-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

```yaml
Type: System.Collections.Generic.List<System.String>
Parameter Sets: NetworkSecurityGroups
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6492c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6492c-130">-PassThru</span></span>
<span data-ttu-id="6492c-131">傳回表示成功或失敗的值</span><span class="sxs-lookup"><span data-stu-id="6492c-131">Return a value indicating success or failure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6492c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6492c-132">CommonParameters</span></span>
<span data-ttu-id="6492c-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6492c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6492c-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6492c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6492c-135">輸入</span><span class="sxs-lookup"><span data-stu-id="6492c-135">INPUTS</span></span>

### <span data-ttu-id="6492c-136">System.object</span><span class="sxs-lookup"><span data-stu-id="6492c-136">System.String</span></span>

### <span data-ttu-id="6492c-137">SecurityCenter AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardeningsRule （）</span><span class="sxs-lookup"><span data-stu-id="6492c-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="6492c-138">輸出</span><span class="sxs-lookup"><span data-stu-id="6492c-138">OUTPUTS</span></span>

### <span data-ttu-id="6492c-139">System.object</span><span class="sxs-lookup"><span data-stu-id="6492c-139">System.Boolean</span></span>

## <span data-ttu-id="6492c-140">筆記</span><span class="sxs-lookup"><span data-stu-id="6492c-140">NOTES</span></span>

## <span data-ttu-id="6492c-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="6492c-141">RELATED LINKS</span></span>