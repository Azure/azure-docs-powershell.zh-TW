---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: f4f2e76a9354ee6ed796b64cbdd83f21d70ff954
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908518"
---
# <span data-ttu-id="24882-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="24882-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="24882-102">簡介</span><span class="sxs-lookup"><span data-stu-id="24882-102">SYNOPSIS</span></span>
<span data-ttu-id="24882-103">取得支援的伺服器變數，以及可用的要求和回應標題。</span><span class="sxs-lookup"><span data-stu-id="24882-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="24882-104">語法</span><span class="sxs-lookup"><span data-stu-id="24882-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="24882-105">描述</span><span class="sxs-lookup"><span data-stu-id="24882-105">DESCRIPTION</span></span>
<span data-ttu-id="24882-106">**Get-AzApplicationGatewayAvailableServerVariableAndHeader Cmdlet** 會取得支援的伺服器變數，以及可用的要求和回應標頭。</span><span class="sxs-lookup"><span data-stu-id="24882-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="24882-107">參數可用來取得變數或標題清單。</span><span class="sxs-lookup"><span data-stu-id="24882-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="24882-108">例子</span><span class="sxs-lookup"><span data-stu-id="24882-108">EXAMPLES</span></span>

### <span data-ttu-id="24882-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="24882-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="24882-110">這個命令會返回所有可用的伺服器變數。</span><span class="sxs-lookup"><span data-stu-id="24882-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="24882-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="24882-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="24882-112">這個命令會返回所有可用的要求標題。</span><span class="sxs-lookup"><span data-stu-id="24882-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="24882-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="24882-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="24882-114">這個命令會返回所有可用的回應標題。</span><span class="sxs-lookup"><span data-stu-id="24882-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="24882-115">範例 4</span><span class="sxs-lookup"><span data-stu-id="24882-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="24882-116">這個命令會返回所有可用的伺服器變數、要求和回應標頭。</span><span class="sxs-lookup"><span data-stu-id="24882-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="24882-117">範例 5</span><span class="sxs-lookup"><span data-stu-id="24882-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="24882-118">這個命令會返回所有可用的伺服器變數、要求和回應標頭。</span><span class="sxs-lookup"><span data-stu-id="24882-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="24882-119">參數</span><span class="sxs-lookup"><span data-stu-id="24882-119">PARAMETERS</span></span>

### <span data-ttu-id="24882-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24882-120">-DefaultProfile</span></span>
<span data-ttu-id="24882-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="24882-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24882-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="24882-122">-RequestHeader</span></span>
<span data-ttu-id="24882-123">應用程式閘道可用的要求標題。</span><span class="sxs-lookup"><span data-stu-id="24882-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="24882-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="24882-124">-ResponseHeader</span></span>
<span data-ttu-id="24882-125">應用程式閘道可用的回應標頭。</span><span class="sxs-lookup"><span data-stu-id="24882-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="24882-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="24882-126">-ServerVariable</span></span>
<span data-ttu-id="24882-127">應用程式閘道可用的伺服器變數。</span><span class="sxs-lookup"><span data-stu-id="24882-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="24882-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24882-128">CommonParameters</span></span>
<span data-ttu-id="24882-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="24882-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24882-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24882-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24882-131">輸入</span><span class="sxs-lookup"><span data-stu-id="24882-131">INPUTS</span></span>

### <span data-ttu-id="24882-132">沒有</span><span class="sxs-lookup"><span data-stu-id="24882-132">None</span></span>

## <span data-ttu-id="24882-133">輸出</span><span class="sxs-lookup"><span data-stu-id="24882-133">OUTPUTS</span></span>

### <span data-ttu-id="24882-134">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span><span class="sxs-lookup"><span data-stu-id="24882-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="24882-135">筆記</span><span class="sxs-lookup"><span data-stu-id="24882-135">NOTES</span></span>
<span data-ttu-id="24882-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** 是 **Get-AzApplicationGatewayAvailableServerVariableAndHeader Cmdlet** 的別名。</span><span class="sxs-lookup"><span data-stu-id="24882-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="24882-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="24882-137">RELATED LINKS</span></span>
