---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: c3ff96a2c1d06fdfba5879244b058ef1a7845f40
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279631"
---
# <span data-ttu-id="505e4-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="505e4-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="505e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="505e4-102">SYNOPSIS</span></span>
<span data-ttu-id="505e4-103">針對防火牆條件建立一個相符變數。</span><span class="sxs-lookup"><span data-stu-id="505e4-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="505e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="505e4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="505e4-105">說明</span><span class="sxs-lookup"><span data-stu-id="505e4-105">DESCRIPTION</span></span>
<span data-ttu-id="505e4-106">**新的-AzApplicationGatewayFirewallMatchVariable** 會針對防火牆條件建立一個相符變數。</span><span class="sxs-lookup"><span data-stu-id="505e4-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="505e4-107">示例</span><span class="sxs-lookup"><span data-stu-id="505e4-107">EXAMPLES</span></span>

### <span data-ttu-id="505e4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="505e4-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="505e4-109">此命令會建立新的 match 變數，且其名稱為 [要求標題]，而選擇器為 [內容長度] 欄位。</span><span class="sxs-lookup"><span data-stu-id="505e4-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="505e4-110">新的 [相符] 變數會儲存在 $variable 中。</span><span class="sxs-lookup"><span data-stu-id="505e4-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="505e4-111">參數</span><span class="sxs-lookup"><span data-stu-id="505e4-111">PARAMETERS</span></span>

### <span data-ttu-id="505e4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="505e4-112">-DefaultProfile</span></span>
<span data-ttu-id="505e4-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="505e4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="505e4-114">-選取器</span><span class="sxs-lookup"><span data-stu-id="505e4-114">-Selector</span></span>
<span data-ttu-id="505e4-115">描述 matchVariable 集合的欄位。</span><span class="sxs-lookup"><span data-stu-id="505e4-115">Describes field of the matchVariable collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505e4-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="505e4-116">-VariableName</span></span>
<span data-ttu-id="505e4-117">[相符] 變數。</span><span class="sxs-lookup"><span data-stu-id="505e4-117">Match Variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RemoteAddr, RequestMethod, QueryString, PostArgs, RequestUri, RequestHeaders, RequestBody, RequestCookies

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="505e4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="505e4-118">CommonParameters</span></span>
<span data-ttu-id="505e4-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="505e4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="505e4-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="505e4-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="505e4-121">輸入</span><span class="sxs-lookup"><span data-stu-id="505e4-121">INPUTS</span></span>

### <span data-ttu-id="505e4-122">所有</span><span class="sxs-lookup"><span data-stu-id="505e4-122">None</span></span>

## <span data-ttu-id="505e4-123">輸出</span><span class="sxs-lookup"><span data-stu-id="505e4-123">OUTPUTS</span></span>

### <span data-ttu-id="505e4-124">PSApplicationGatewayFirewallMatchVariable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="505e4-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="505e4-125">筆記</span><span class="sxs-lookup"><span data-stu-id="505e4-125">NOTES</span></span>

## <span data-ttu-id="505e4-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="505e4-126">RELATED LINKS</span></span>
