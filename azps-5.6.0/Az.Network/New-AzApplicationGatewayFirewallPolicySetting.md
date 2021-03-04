---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: 256509a42b844b196728b89b30abcdb6c5b9b386
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904606"
---
# <span data-ttu-id="da1f0-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="da1f0-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="da1f0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="da1f0-102">SYNOPSIS</span></span>
<span data-ttu-id="da1f0-103">建立防火牆策略的設定</span><span class="sxs-lookup"><span data-stu-id="da1f0-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="da1f0-104">語法</span><span class="sxs-lookup"><span data-stu-id="da1f0-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da1f0-105">描述</span><span class="sxs-lookup"><span data-stu-id="da1f0-105">DESCRIPTION</span></span>
<span data-ttu-id="da1f0-106">**New-AzApplicationGatewayFirewallPolicySetting** 會為防火牆策略建立一個策略設定。</span><span class="sxs-lookup"><span data-stu-id="da1f0-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="da1f0-107">例子</span><span class="sxs-lookup"><span data-stu-id="da1f0-107">EXAMPLES</span></span>

### <span data-ttu-id="da1f0-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="da1f0-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="da1f0-109">命令會建立一個以 $enabledState、模式為 $enabledMode、RequestBodyCheck 為 false、FileUploadLimitInMb 為 $fileUploadLimitInMb 且 MaxRequestBodySizeInKb 為 $$maxRequestBodySizeInKb。</span><span class="sxs-lookup"><span data-stu-id="da1f0-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="da1f0-110">新的 policySettings 會儲存到$condition。</span><span class="sxs-lookup"><span data-stu-id="da1f0-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="da1f0-111">參數</span><span class="sxs-lookup"><span data-stu-id="da1f0-111">PARAMETERS</span></span>

### <span data-ttu-id="da1f0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da1f0-112">-DefaultProfile</span></span>
<span data-ttu-id="da1f0-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="da1f0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da1f0-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="da1f0-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="da1f0-115">在防火牆政策設定中修改要求BodyCheck。</span><span class="sxs-lookup"><span data-stu-id="da1f0-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="da1f0-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="da1f0-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="da1f0-117">檔案Upload 大小上限 ，以 MB 為單位。</span><span class="sxs-lookup"><span data-stu-id="da1f0-117">Maximum fileUpload size in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1f0-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="da1f0-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="da1f0-119">防火牆政策設定中的 MaxRequestBodySizeInKb。</span><span class="sxs-lookup"><span data-stu-id="da1f0-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 128
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1f0-120">-模式</span><span class="sxs-lookup"><span data-stu-id="da1f0-120">-Mode</span></span>
<span data-ttu-id="da1f0-121">防火牆政策設定中的防火牆模式。</span><span class="sxs-lookup"><span data-stu-id="da1f0-121">Firewall Mode in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: Detection
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1f0-122">-State</span><span class="sxs-lookup"><span data-stu-id="da1f0-122">-State</span></span>
<span data-ttu-id="da1f0-123">防火牆政策設定中的狀態變數。</span><span class="sxs-lookup"><span data-stu-id="da1f0-123">State variable in policy settings of the firewall policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: False
Position: Named
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da1f0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da1f0-124">CommonParameters</span></span>
<span data-ttu-id="da1f0-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="da1f0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da1f0-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da1f0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da1f0-127">輸入</span><span class="sxs-lookup"><span data-stu-id="da1f0-127">INPUTS</span></span>

### <span data-ttu-id="da1f0-128">沒有</span><span class="sxs-lookup"><span data-stu-id="da1f0-128">None</span></span>

## <span data-ttu-id="da1f0-129">輸出</span><span class="sxs-lookup"><span data-stu-id="da1f0-129">OUTPUTS</span></span>

### <span data-ttu-id="da1f0-130">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="da1f0-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="da1f0-131">筆記</span><span class="sxs-lookup"><span data-stu-id="da1f0-131">NOTES</span></span>

## <span data-ttu-id="da1f0-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="da1f0-132">RELATED LINKS</span></span>
