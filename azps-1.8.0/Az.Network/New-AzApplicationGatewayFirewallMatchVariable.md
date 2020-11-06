---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallmatchvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallMatchVariable.md
ms.openlocfilehash: 05a1929f79799be8006ae82c4948dc0a81839040
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621860"
---
# <span data-ttu-id="d4f02-101">New-AzApplicationGatewayFirewallMatchVariable</span><span class="sxs-lookup"><span data-stu-id="d4f02-101">New-AzApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="d4f02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4f02-102">SYNOPSIS</span></span>
<span data-ttu-id="d4f02-103">針對防火牆條件建立一個相符變數。</span><span class="sxs-lookup"><span data-stu-id="d4f02-103">Creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="d4f02-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4f02-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallMatchVariable -VariableName <String> [-Selector <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4f02-105">說明</span><span class="sxs-lookup"><span data-stu-id="d4f02-105">DESCRIPTION</span></span>
<span data-ttu-id="d4f02-106">**新的-AzApplicationGatewayFirewallMatchVariable** 會針對防火牆條件建立一個相符變數。</span><span class="sxs-lookup"><span data-stu-id="d4f02-106">The **New-AzApplicationGatewayFirewallMatchVariable** creates a match variable for firewall condition.</span></span>

## <span data-ttu-id="d4f02-107">示例</span><span class="sxs-lookup"><span data-stu-id="d4f02-107">EXAMPLES</span></span>

### <span data-ttu-id="d4f02-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d4f02-108">Example 1</span></span>
```powershell
PS C:\> $variable = New-AzureRmApplicationGatewayFirewallMatchVariable -VariableName RequestHeaders -Selector Content-Length
```

<span data-ttu-id="d4f02-109">此命令會建立新的 match 變數，且其名稱為 [要求標題]，而選擇器為 [內容長度] 欄位。</span><span class="sxs-lookup"><span data-stu-id="d4f02-109">The command creates a new match variable with name of request headers and selector is Content-Length field.</span></span> <span data-ttu-id="d4f02-110">新的 [相符] 變數會儲存在 $variable 中。</span><span class="sxs-lookup"><span data-stu-id="d4f02-110">The new match variable is saved in $variable.</span></span>

## <span data-ttu-id="d4f02-111">參數</span><span class="sxs-lookup"><span data-stu-id="d4f02-111">PARAMETERS</span></span>

### <span data-ttu-id="d4f02-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4f02-112">-DefaultProfile</span></span>
<span data-ttu-id="d4f02-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4f02-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4f02-114">-選取器</span><span class="sxs-lookup"><span data-stu-id="d4f02-114">-Selector</span></span>
<span data-ttu-id="d4f02-115">描述 matchVariable 集合的欄位。</span><span class="sxs-lookup"><span data-stu-id="d4f02-115">Describes field of the matchVariable collection.</span></span>

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

### <span data-ttu-id="d4f02-116">-VariableName</span><span class="sxs-lookup"><span data-stu-id="d4f02-116">-VariableName</span></span>
<span data-ttu-id="d4f02-117">[相符] 變數。</span><span class="sxs-lookup"><span data-stu-id="d4f02-117">Match Variable.</span></span>

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

### <span data-ttu-id="d4f02-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4f02-118">CommonParameters</span></span>
<span data-ttu-id="d4f02-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4f02-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4f02-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d4f02-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4f02-121">輸入</span><span class="sxs-lookup"><span data-stu-id="d4f02-121">INPUTS</span></span>

### <span data-ttu-id="d4f02-122">所有</span><span class="sxs-lookup"><span data-stu-id="d4f02-122">None</span></span>

## <span data-ttu-id="d4f02-123">輸出</span><span class="sxs-lookup"><span data-stu-id="d4f02-123">OUTPUTS</span></span>

### <span data-ttu-id="d4f02-124">PSApplicationGatewayFirewallMatchVariable 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d4f02-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallMatchVariable</span></span>

## <span data-ttu-id="d4f02-125">筆記</span><span class="sxs-lookup"><span data-stu-id="d4f02-125">NOTES</span></span>

## <span data-ttu-id="d4f02-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4f02-126">RELATED LINKS</span></span>
