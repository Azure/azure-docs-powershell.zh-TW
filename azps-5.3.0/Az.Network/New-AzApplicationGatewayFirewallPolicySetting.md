---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicysetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicySetting.md
ms.openlocfilehash: b1665975fd85268bdb8788eb96ba0c8694b6f4c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98288756"
---
# <span data-ttu-id="2e81d-101">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="2e81d-101">New-AzApplicationGatewayFirewallPolicySetting</span></span>

## <span data-ttu-id="2e81d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e81d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e81d-103">建立防火牆原則的原則設定</span><span class="sxs-lookup"><span data-stu-id="2e81d-103">Creates a policy setting for the firewall policy</span></span>

## <span data-ttu-id="2e81d-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e81d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicySetting [-Mode <String>] [-State <String>] [-DisableRequestBodyCheck]
 [-MaxRequestBodySizeInKb <Int32>] [-MaxFileUploadInMb <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e81d-105">說明</span><span class="sxs-lookup"><span data-stu-id="2e81d-105">DESCRIPTION</span></span>
<span data-ttu-id="2e81d-106">[ **新-AzApplicationGatewayFirewallPolicySetting** ] 會建立防火牆原則的原則設定。</span><span class="sxs-lookup"><span data-stu-id="2e81d-106">The **New-AzApplicationGatewayFirewallPolicySetting** creates a policy settings for a firewall policy.</span></span>

## <span data-ttu-id="2e81d-107">示例</span><span class="sxs-lookup"><span data-stu-id="2e81d-107">EXAMPLES</span></span>

### <span data-ttu-id="2e81d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="2e81d-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicySetting -State $enabledState -Mode $enabledMode -DisableRequestBodyCheck -MaxFileUploadInMb $fileUploadLimitInMb -MaxRequestBodySizeInKb $maxRequestBodySizeInKb
```

<span data-ttu-id="2e81d-109">此命令會建立一個策略設定，並將狀態設為 $enabledState、模式為 $enabledMode、RequestBodyCheck 為 false、FileUploadLimitInMb 為 $fileUploadLimitInMb，而 MaxRequestBodySizeInKb 為 $ $maxRequestBodySizeInKb。</span><span class="sxs-lookup"><span data-stu-id="2e81d-109">The command creates a policy setting with state as $enabledState, mode as $enabledMode, RequestBodyCheck as false, FileUploadLimitInMb as $fileUploadLimitInMb and MaxRequestBodySizeInKb as $$maxRequestBodySizeInKb.</span></span>
<span data-ttu-id="2e81d-110">新的 policySettings 會儲存到 $condition。</span><span class="sxs-lookup"><span data-stu-id="2e81d-110">The new policySettings is stored to $condition.</span></span>

## <span data-ttu-id="2e81d-111">參數</span><span class="sxs-lookup"><span data-stu-id="2e81d-111">PARAMETERS</span></span>

### <span data-ttu-id="2e81d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e81d-112">-DefaultProfile</span></span>
<span data-ttu-id="2e81d-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2e81d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e81d-114">-DisableRequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="2e81d-114">-DisableRequestBodyCheck</span></span>
<span data-ttu-id="2e81d-115">Diables 防火牆原則的原則設定中的 requestBodyCheck。</span><span class="sxs-lookup"><span data-stu-id="2e81d-115">Diables the requestBodyCheck in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="2e81d-116">-MaxFileUploadInMb</span><span class="sxs-lookup"><span data-stu-id="2e81d-116">-MaxFileUploadInMb</span></span>
<span data-ttu-id="2e81d-117">最大 fileUpload 大小（MB）。</span><span class="sxs-lookup"><span data-stu-id="2e81d-117">Maximum fileUpload size in MB.</span></span>

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

### <span data-ttu-id="2e81d-118">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="2e81d-118">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="2e81d-119">在防火牆原則的原則設定中 MaxRequestBodySizeInKb。</span><span class="sxs-lookup"><span data-stu-id="2e81d-119">MaxRequestBodySizeInKb in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="2e81d-120">模式</span><span class="sxs-lookup"><span data-stu-id="2e81d-120">-Mode</span></span>
<span data-ttu-id="2e81d-121">防火牆原則的原則設定中的防火牆模式。</span><span class="sxs-lookup"><span data-stu-id="2e81d-121">Firewall Mode in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="2e81d-122">-State</span><span class="sxs-lookup"><span data-stu-id="2e81d-122">-State</span></span>
<span data-ttu-id="2e81d-123">防火牆原則的原則設定中的狀態變數。</span><span class="sxs-lookup"><span data-stu-id="2e81d-123">State variable in policy settings of the firewall policy.</span></span>

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

### <span data-ttu-id="2e81d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e81d-124">CommonParameters</span></span>
<span data-ttu-id="2e81d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e81d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e81d-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2e81d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e81d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2e81d-127">INPUTS</span></span>

### <span data-ttu-id="2e81d-128">所有</span><span class="sxs-lookup"><span data-stu-id="2e81d-128">None</span></span>

## <span data-ttu-id="2e81d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2e81d-129">OUTPUTS</span></span>

### <span data-ttu-id="2e81d-130">PSApplicationGatewayFirewallPolicySettings 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2e81d-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

## <span data-ttu-id="2e81d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2e81d-131">NOTES</span></span>

## <span data-ttu-id="2e81d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e81d-132">RELATED LINKS</span></span>
