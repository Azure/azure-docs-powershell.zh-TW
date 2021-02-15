---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionsignatureoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionSignatureOverride.md
ms.openlocfilehash: d2389a8d4880b576e51cda41ac3c15bd091257c1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131250"
---
# <span data-ttu-id="76730-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span><span class="sxs-lookup"><span data-stu-id="76730-101">New-AzFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="76730-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76730-102">SYNOPSIS</span></span>
<span data-ttu-id="76730-103">建立新的 Azure 防火牆原則入侵偵測簽名覆蓋</span><span class="sxs-lookup"><span data-stu-id="76730-103">Creates a new Azure Firewall Policy Intrusion Detection Signature Override</span></span>

## <span data-ttu-id="76730-104">句法</span><span class="sxs-lookup"><span data-stu-id="76730-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id <UInt64> -Mode <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76730-105">說明</span><span class="sxs-lookup"><span data-stu-id="76730-105">DESCRIPTION</span></span>
<span data-ttu-id="76730-106">**新的-AzFirewallPolicyIntrusionDetectionSignatureOverride** Cmdlet 會建立 Azure 防火牆原則簽名覆蓋物件。</span><span class="sxs-lookup"><span data-stu-id="76730-106">The **New-AzFirewallPolicyIntrusionDetectionSignatureOverride** cmdlet creates an Azure Firewall Policy Signature Override Object.</span></span>

## <span data-ttu-id="76730-107">示例</span><span class="sxs-lookup"><span data-stu-id="76730-107">EXAMPLES</span></span>

### <span data-ttu-id="76730-108">範例 1: 1。</span><span class="sxs-lookup"><span data-stu-id="76730-108">Example 1: 1.</span></span> <span data-ttu-id="76730-109">使用簽名覆蓋來建立入侵偵測</span><span class="sxs-lookup"><span data-stu-id="76730-109">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```
<span data-ttu-id="76730-110">這個範例會使用特定的簽章覆蓋來建立 [拒絕] 模式的入侵偵測</span><span class="sxs-lookup"><span data-stu-id="76730-110">This example creates intrusion detection with specific signature override to Deny mode</span></span>

## <span data-ttu-id="76730-111">參數</span><span class="sxs-lookup"><span data-stu-id="76730-111">PARAMETERS</span></span>

### <span data-ttu-id="76730-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76730-112">-DefaultProfile</span></span>
<span data-ttu-id="76730-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="76730-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76730-114">-識別碼</span><span class="sxs-lookup"><span data-stu-id="76730-114">-Id</span></span>
<span data-ttu-id="76730-115">簽名 id。</span><span class="sxs-lookup"><span data-stu-id="76730-115">Signature id.</span></span>

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

### <span data-ttu-id="76730-116">模式</span><span class="sxs-lookup"><span data-stu-id="76730-116">-Mode</span></span>
<span data-ttu-id="76730-117">簽名狀態。</span><span class="sxs-lookup"><span data-stu-id="76730-117">Signature state.</span></span>

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

### <span data-ttu-id="76730-118">-確認</span><span class="sxs-lookup"><span data-stu-id="76730-118">-Confirm</span></span>
<span data-ttu-id="76730-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="76730-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76730-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76730-120">-WhatIf</span></span>
<span data-ttu-id="76730-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76730-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76730-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76730-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76730-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76730-123">CommonParameters</span></span>
<span data-ttu-id="76730-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76730-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76730-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="76730-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76730-126">輸入</span><span class="sxs-lookup"><span data-stu-id="76730-126">INPUTS</span></span>

### <span data-ttu-id="76730-127">所有</span><span class="sxs-lookup"><span data-stu-id="76730-127">None</span></span>

## <span data-ttu-id="76730-128">輸出</span><span class="sxs-lookup"><span data-stu-id="76730-128">OUTPUTS</span></span>

### <span data-ttu-id="76730-129">PSAzureFirewallPolicyIntrusionDetectionSignatureOverride 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="76730-129">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionSignatureOverride</span></span>

## <span data-ttu-id="76730-130">筆記</span><span class="sxs-lookup"><span data-stu-id="76730-130">NOTES</span></span>

## <span data-ttu-id="76730-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="76730-131">RELATED LINKS</span></span>
