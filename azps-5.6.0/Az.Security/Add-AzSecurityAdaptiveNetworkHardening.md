---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: e0e634a4947953f65c3fd68c9cc3e40dfca17fd2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907054"
---
# <span data-ttu-id="c4dbb-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="c4dbb-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="c4dbb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c4dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="c4dbb-103">在要求中列出的 NSG (上) 規則</span><span class="sxs-lookup"><span data-stu-id="c4dbb-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="c4dbb-104">語法</span><span class="sxs-lookup"><span data-stu-id="c4dbb-104">SYNTAX</span></span>

### <span data-ttu-id="c4dbb-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="c4dbb-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4dbb-106">描述</span><span class="sxs-lookup"><span data-stu-id="c4dbb-106">DESCRIPTION</span></span>
<span data-ttu-id="c4dbb-107">Azure 資訊安全中心會自動計算自適性網路轉切，使用此 Cmdlet 在要求中列出的 NSG (上) 規則。</span><span class="sxs-lookup"><span data-stu-id="c4dbb-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="c4dbb-108">例子</span><span class="sxs-lookup"><span data-stu-id="c4dbb-108">EXAMPLES</span></span>

### <span data-ttu-id="c4dbb-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="c4dbb-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="c4dbb-110">在要求中列出的 NSG (上) 規則</span><span class="sxs-lookup"><span data-stu-id="c4dbb-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="c4dbb-111">參數</span><span class="sxs-lookup"><span data-stu-id="c4dbb-111">PARAMETERS</span></span>

### <span data-ttu-id="c4dbb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4dbb-112">-DefaultProfile</span></span>
<span data-ttu-id="c4dbb-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4dbb-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4dbb-114">-AdaptiveNetwork1eningResourceName</span><span class="sxs-lookup"><span data-stu-id="c4dbb-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="c4dbb-115">自適性網路增強資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4dbb-115">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="c4dbb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4dbb-116">-ResourceGroupName</span></span>
<span data-ttu-id="c4dbb-117">資源組名。</span><span class="sxs-lookup"><span data-stu-id="c4dbb-117">Resource group name.</span></span>

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

### <span data-ttu-id="c4dbb-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c4dbb-118">-ResourceName</span></span>
<span data-ttu-id="c4dbb-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c4dbb-119">Resource name.</span></span>

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

### <span data-ttu-id="c4dbb-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="c4dbb-120">-ResourceNamespace</span></span>
<span data-ttu-id="c4dbb-121">資源的命名空間。</span><span class="sxs-lookup"><span data-stu-id="c4dbb-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="c4dbb-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c4dbb-122">-ResourceType</span></span>
<span data-ttu-id="c4dbb-123">資源的類型。</span><span class="sxs-lookup"><span data-stu-id="c4dbb-123">The type of the resource.</span></span>

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

### <span data-ttu-id="c4dbb-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c4dbb-124">-SubscriptionId</span></span>
<span data-ttu-id="c4dbb-125">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="c4dbb-125">Azure subscription ID.</span></span>

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

### <span data-ttu-id="c4dbb-126">-規則</span><span class="sxs-lookup"><span data-stu-id="c4dbb-126">-Rules</span></span>
<span data-ttu-id="c4dbb-127">要強制執行的規則。</span><span class="sxs-lookup"><span data-stu-id="c4dbb-127">The rules to enforce.</span></span>

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

### <span data-ttu-id="c4dbb-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="c4dbb-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="c4dbb-129">有效網路安全性群組 Azure 資源識別碼，將會更新自自適性網路增強規則所建立的安全性規則。</span><span class="sxs-lookup"><span data-stu-id="c4dbb-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

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

### <span data-ttu-id="c4dbb-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4dbb-130">-PassThru</span></span>
<span data-ttu-id="c4dbb-131">返回指出成功或失敗的值</span><span class="sxs-lookup"><span data-stu-id="c4dbb-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="c4dbb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4dbb-132">CommonParameters</span></span>
<span data-ttu-id="c4dbb-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c4dbb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4dbb-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c4dbb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4dbb-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c4dbb-135">INPUTS</span></span>

### <span data-ttu-id="c4dbb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c4dbb-136">System.String</span></span>

### <span data-ttu-id="c4dbb-137">Microsoft.Azure.Commands.SecurityCenter.models.AdaptiveNetworkWorkEnings.PSSecurityAdaptiveNetworkWorkWorkEningsRule</span><span class="sxs-lookup"><span data-stu-id="c4dbb-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="c4dbb-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c4dbb-138">OUTPUTS</span></span>

### <span data-ttu-id="c4dbb-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c4dbb-139">System.Boolean</span></span>

## <span data-ttu-id="c4dbb-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c4dbb-140">NOTES</span></span>

## <span data-ttu-id="c4dbb-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4dbb-141">RELATED LINKS</span></span>