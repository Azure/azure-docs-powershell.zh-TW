---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionsignatureoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
ms.openlocfilehash: c6aa2bb9bf3866e35ad59e59bdf5ded333fd2816
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916911"
---
# <span data-ttu-id="f7e1a-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="f7e1a-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="f7e1a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7e1a-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e1a-103">建立新的 Azure 防火牆策略入侵偵測簽章取代</span><span class="sxs-lookup"><span data-stu-id="f7e1a-103">Creates a new Azure Firewall Policy Intrusion Detection Signature Override</span></span>

## <span data-ttu-id="f7e1a-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7e1a-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id <UInt64> -Mode <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7e1a-105">描述</span><span class="sxs-lookup"><span data-stu-id="f7e1a-105">DESCRIPTION</span></span>
<span data-ttu-id="f7e1a-106">**New-AzFirewallPolicyIntrusionDetectionSignatureOverride** Cmdlet 會建立 Azure 防火牆策略簽名 Override 物件。</span><span class="sxs-lookup"><span data-stu-id="f7e1a-106">The **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cmdlet creates an Azure Firewall Policy Signature Override Object.</span></span>

## <span data-ttu-id="f7e1a-107">例子</span><span class="sxs-lookup"><span data-stu-id="f7e1a-107">EXAMPLES</span></span>

### <span data-ttu-id="f7e1a-108">範例 1：1。</span><span class="sxs-lookup"><span data-stu-id="f7e1a-108">Example 1: 1.</span></span> <span data-ttu-id="f7e1a-109">使用簽章覆蓋建立入侵偵測</span><span class="sxs-lookup"><span data-stu-id="f7e1a-109">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```
<span data-ttu-id="f7e1a-110">此範例會建立入侵偵測，將特定的簽章取代為拒絕模式</span><span class="sxs-lookup"><span data-stu-id="f7e1a-110">This example creates intrusion detection with specific signature override to Deny mode</span></span>

## <span data-ttu-id="f7e1a-111">參數</span><span class="sxs-lookup"><span data-stu-id="f7e1a-111">PARAMETERS</span></span>

### <span data-ttu-id="f7e1a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e1a-112">-DefaultProfile</span></span>
<span data-ttu-id="f7e1a-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7e1a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e1a-114">-Id</span><span class="sxs-lookup"><span data-stu-id="f7e1a-114">-Id</span></span>
<span data-ttu-id="f7e1a-115">簽章識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7e1a-115">Signature id.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e1a-116">-模式</span><span class="sxs-lookup"><span data-stu-id="f7e1a-116">-Mode</span></span>
<span data-ttu-id="f7e1a-117">簽章狀態。</span><span class="sxs-lookup"><span data-stu-id="f7e1a-117">Signature state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e1a-118">-確認</span><span class="sxs-lookup"><span data-stu-id="f7e1a-118">-Confirm</span></span>
<span data-ttu-id="f7e1a-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f7e1a-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e1a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7e1a-120">-WhatIf</span></span>
<span data-ttu-id="f7e1a-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7e1a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7e1a-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7e1a-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7e1a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e1a-123">CommonParameters</span></span>
<span data-ttu-id="f7e1a-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7e1a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e1a-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7e1a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e1a-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f7e1a-126">INPUTS</span></span>

### <span data-ttu-id="f7e1a-127">沒有</span><span class="sxs-lookup"><span data-stu-id="f7e1a-127">None</span></span>

## <span data-ttu-id="f7e1a-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f7e1a-128">OUTPUTS</span></span>

### <span data-ttu-id="f7e1a-129">Microsoft.Azure.Commands.Network.models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="f7e1a-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="f7e1a-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f7e1a-130">NOTES</span></span>

## <span data-ttu-id="f7e1a-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7e1a-131">RELATED LINKS</span></span>
