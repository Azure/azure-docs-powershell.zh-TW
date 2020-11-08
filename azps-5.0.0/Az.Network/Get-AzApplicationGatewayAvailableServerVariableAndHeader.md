---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailableservervariableandheader
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableServerVariableAndHeader.md
ms.openlocfilehash: 8fb1f76b32332c7679ef59f50123072311de86fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139808"
---
# <span data-ttu-id="469e4-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span><span class="sxs-lookup"><span data-stu-id="469e4-101">Get-AzApplicationGatewayAvailableServerVariableAndHeader</span></span>

## <span data-ttu-id="469e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="469e4-102">SYNOPSIS</span></span>
<span data-ttu-id="469e4-103">取得支援的伺服器變數，以及可用的要求與回應標頭。</span><span class="sxs-lookup"><span data-stu-id="469e4-103">Get the supported server variables and available request and response headers.</span></span>

## <span data-ttu-id="469e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="469e4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableServerVariableAndHeader [-DefaultProfile <IAzureContextContainer>]
 [-ServerVariable] [-RequestHeader] [-ResponseHeader] [<CommonParameters>]
```

## <span data-ttu-id="469e4-105">說明</span><span class="sxs-lookup"><span data-stu-id="469e4-105">DESCRIPTION</span></span>
<span data-ttu-id="469e4-106">**AzApplicationGatewayAvailableServerVariableAndHeader** Cmdlet 會取得支援的伺服器變數，以及可用的要求與回應標頭。</span><span class="sxs-lookup"><span data-stu-id="469e4-106">The **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet gets the supported server variables and available request and response headers.</span></span> <span data-ttu-id="469e4-107">參數可以用來取得變數或標題清單。</span><span class="sxs-lookup"><span data-stu-id="469e4-107">Parameters can be used to get the variables or headers lists.</span></span>

## <span data-ttu-id="469e4-108">示例</span><span class="sxs-lookup"><span data-stu-id="469e4-108">EXAMPLES</span></span>

### <span data-ttu-id="469e4-109">範例1</span><span class="sxs-lookup"><span data-stu-id="469e4-109">Example 1</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ServerVariable
```

<span data-ttu-id="469e4-110">這個命令會傳回所有可用的伺服器變數。</span><span class="sxs-lookup"><span data-stu-id="469e4-110">This commands returns all the available server variables.</span></span>

### <span data-ttu-id="469e4-111">範例2</span><span class="sxs-lookup"><span data-stu-id="469e4-111">Example 2</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -RequestHeader
```

<span data-ttu-id="469e4-112">這個命令會傳回所有可用的要求標頭。</span><span class="sxs-lookup"><span data-stu-id="469e4-112">This commands returns all the available request headers.</span></span>

### <span data-ttu-id="469e4-113">範例3</span><span class="sxs-lookup"><span data-stu-id="469e4-113">Example 3</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader -ResponseHeader
```

<span data-ttu-id="469e4-114">這個命令會傳回所有可用的回應標頭。</span><span class="sxs-lookup"><span data-stu-id="469e4-114">This commands returns all the available response headers.</span></span>

### <span data-ttu-id="469e4-115">範例4</span><span class="sxs-lookup"><span data-stu-id="469e4-115">Example 4</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader - ServerVariable -RequestHeader -ResponseHeader
```

<span data-ttu-id="469e4-116">這個命令會傳回所有可用的伺服器變數、要求和回應標頭。</span><span class="sxs-lookup"><span data-stu-id="469e4-116">This commands returns all the available server variables, request and response headers.</span></span>

### <span data-ttu-id="469e4-117">範例5</span><span class="sxs-lookup"><span data-stu-id="469e4-117">Example 5</span></span>
```
PS C:\>Get-AzApplicationGatewayAvailableServerVariableAndHeader
```

<span data-ttu-id="469e4-118">這個命令會傳回所有可用的伺服器變數、要求和回應標頭。</span><span class="sxs-lookup"><span data-stu-id="469e4-118">This commands returns all the available server variables, request and response headers.</span></span>

## <span data-ttu-id="469e4-119">參數</span><span class="sxs-lookup"><span data-stu-id="469e4-119">PARAMETERS</span></span>

### <span data-ttu-id="469e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="469e4-120">-DefaultProfile</span></span>
<span data-ttu-id="469e4-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="469e4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="469e4-122">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="469e4-122">-RequestHeader</span></span>
<span data-ttu-id="469e4-123">應用程式閘道可用的要求標頭。</span><span class="sxs-lookup"><span data-stu-id="469e4-123">Application Gateway available request headers.</span></span>

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

### <span data-ttu-id="469e4-124">-ResponseHeader</span><span class="sxs-lookup"><span data-stu-id="469e4-124">-ResponseHeader</span></span>
<span data-ttu-id="469e4-125">應用程式閘道可用的回應標頭。</span><span class="sxs-lookup"><span data-stu-id="469e4-125">Application Gateway available response headers.</span></span>

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

### <span data-ttu-id="469e4-126">-ServerVariable</span><span class="sxs-lookup"><span data-stu-id="469e4-126">-ServerVariable</span></span>
<span data-ttu-id="469e4-127">應用程式閘道可用的伺服器變數。</span><span class="sxs-lookup"><span data-stu-id="469e4-127">Application Gateway available server variables.</span></span>

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

### <span data-ttu-id="469e4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="469e4-128">CommonParameters</span></span>
<span data-ttu-id="469e4-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="469e4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="469e4-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="469e4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="469e4-131">輸入</span><span class="sxs-lookup"><span data-stu-id="469e4-131">INPUTS</span></span>

### <span data-ttu-id="469e4-132">所有</span><span class="sxs-lookup"><span data-stu-id="469e4-132">None</span></span>

## <span data-ttu-id="469e4-133">輸出</span><span class="sxs-lookup"><span data-stu-id="469e4-133">OUTPUTS</span></span>

### <span data-ttu-id="469e4-134">PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="469e4-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableServerVariableAndRequestHeaderResult</span></span>

## <span data-ttu-id="469e4-135">筆記</span><span class="sxs-lookup"><span data-stu-id="469e4-135">NOTES</span></span>
<span data-ttu-id="469e4-136">**清單-AzApplicationGatewayAvailableServerVariableAndHeader** 是 **AzApplicationGatewayAvailableServerVariableAndHeader** Cmdlet 的別名。</span><span class="sxs-lookup"><span data-stu-id="469e4-136">**List-AzApplicationGatewayAvailableServerVariableAndHeader** is an alias for the **Get-AzApplicationGatewayAvailableServerVariableAndHeader** cmdlet.</span></span>

## <span data-ttu-id="469e4-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="469e4-137">RELATED LINKS</span></span>
