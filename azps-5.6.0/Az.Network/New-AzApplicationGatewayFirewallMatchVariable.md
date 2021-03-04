---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: 824c1c4e98fca6b6f7d2ff3df9217cb000eeaf21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917689"
---
# <span data-ttu-id="56263-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="56263-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="56263-102">簡介</span><span class="sxs-lookup"><span data-stu-id="56263-102">SYNOPSIS</span></span>
<span data-ttu-id="56263-103">建立防火牆條件的比對變數。</span><span class="sxs-lookup"><span data-stu-id="56263-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="56263-104">語法</span><span class="sxs-lookup"><span data-stu-id="56263-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56263-105">描述</span><span class="sxs-lookup"><span data-stu-id="56263-105">DESCRIPTION</span></span>
<span data-ttu-id="56263-106">**New-AzApplicationGatewayFirewallMatchVariable** 會針對防火牆條件建立相符變數。</span><span class="sxs-lookup"><span data-stu-id="56263-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="56263-107">例子</span><span class="sxs-lookup"><span data-stu-id="56263-107">EXAMPLES</span></span>

### <span data-ttu-id="56263-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="56263-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="56263-109">命令會建立一個新的比對變數，其中要求標題和選取器的名稱是 Content-Length 欄位。</span><span class="sxs-lookup"><span data-stu-id="56263-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="56263-110">新的比對變數會儲存于$variable。</span><span class="sxs-lookup"><span data-stu-id="56263-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="56263-111">參數</span><span class="sxs-lookup"><span data-stu-id="56263-111">PARAMETERS</span></span>

### <span data-ttu-id="56263-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56263-112">-DefaultProfile</span></span>
<span data-ttu-id="56263-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="56263-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56263-114">-選取器</span><span class="sxs-lookup"><span data-stu-id="56263-114">-Selector</span></span>
<span data-ttu-id="56263-115">描述 matchVariable 集合的欄位。</span><span class="sxs-lookup"><span data-stu-id="56263-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="56263-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="56263-116">-VariableName</span></span>
<span data-ttu-id="56263-117">Match Variable。</span><span class="sxs-lookup"><span data-stu-id="56263-117">Match Variable.</span></span>

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

### <span data-ttu-id="56263-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56263-118">CommonParameters</span></span>
<span data-ttu-id="56263-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="56263-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56263-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="56263-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56263-121">輸入</span><span class="sxs-lookup"><span data-stu-id="56263-121">INPUTS</span></span>

### <span data-ttu-id="56263-122">沒有</span><span class="sxs-lookup"><span data-stu-id="56263-122">None</span></span>

## <span data-ttu-id="56263-123">輸出</span><span class="sxs-lookup"><span data-stu-id="56263-123">OUTPUTS</span></span>

### <span data-ttu-id="56263-124">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="56263-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="56263-125">筆記</span><span class="sxs-lookup"><span data-stu-id="56263-125">NOTES</span></span>

## <span data-ttu-id="56263-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="56263-126">RELATED LINKS</span></span>
