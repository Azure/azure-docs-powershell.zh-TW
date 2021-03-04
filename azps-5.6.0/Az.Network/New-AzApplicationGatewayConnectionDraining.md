---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b5bfedea118aa3770bac3141d05db379a4655906
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916009"
---
# <span data-ttu-id="8bd0e-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="8bd0e-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="8bd0e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8bd0e-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd0e-103">為後端 HTTP 設定建立新的連接耗用設定。</span><span class="sxs-lookup"><span data-stu-id="8bd0e-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="8bd0e-104">語法</span><span class="sxs-lookup"><span data-stu-id="8bd0e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bd0e-105">描述</span><span class="sxs-lookup"><span data-stu-id="8bd0e-105">DESCRIPTION</span></span>
<span data-ttu-id="8bd0e-106">**New-AzApplicationGatewayConnectionDraining** Cmdlet 為後端 HTTP 設定建立新的連接消耗設定。</span><span class="sxs-lookup"><span data-stu-id="8bd0e-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="8bd0e-107">例子</span><span class="sxs-lookup"><span data-stu-id="8bd0e-107">EXAMPLES</span></span>

### <span data-ttu-id="8bd0e-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="8bd0e-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="8bd0e-109">此命令會建立新的連接耗用設定，將 Enabled 設定為 True 且 DrainTimeoutInSec 設定為 42 秒，並儲存于 $connectionDraining。</span><span class="sxs-lookup"><span data-stu-id="8bd0e-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="8bd0e-110">參數</span><span class="sxs-lookup"><span data-stu-id="8bd0e-110">PARAMETERS</span></span>

### <span data-ttu-id="8bd0e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd0e-111">-DefaultProfile</span></span>
<span data-ttu-id="8bd0e-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8bd0e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bd0e-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="8bd0e-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="8bd0e-114">連接漏掉的秒數為使用中。</span><span class="sxs-lookup"><span data-stu-id="8bd0e-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="8bd0e-115">可接受的值為 1 秒到 3600 秒。</span><span class="sxs-lookup"><span data-stu-id="8bd0e-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd0e-116">-已啟用</span><span class="sxs-lookup"><span data-stu-id="8bd0e-116">-Enabled</span></span>
<span data-ttu-id="8bd0e-117">是否已啟用連接耗用。</span><span class="sxs-lookup"><span data-stu-id="8bd0e-117">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bd0e-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd0e-118">CommonParameters</span></span>
<span data-ttu-id="8bd0e-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8bd0e-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd0e-120">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8bd0e-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd0e-121">輸入</span><span class="sxs-lookup"><span data-stu-id="8bd0e-121">INPUTS</span></span>

### <span data-ttu-id="8bd0e-122">沒有</span><span class="sxs-lookup"><span data-stu-id="8bd0e-122">None</span></span>

## <span data-ttu-id="8bd0e-123">輸出</span><span class="sxs-lookup"><span data-stu-id="8bd0e-123">OUTPUTS</span></span>

### <span data-ttu-id="8bd0e-124">Microsoft.Azure.Commands.Network.models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="8bd0e-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="8bd0e-125">筆記</span><span class="sxs-lookup"><span data-stu-id="8bd0e-125">NOTES</span></span>

## <span data-ttu-id="8bd0e-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="8bd0e-126">RELATED LINKS</span></span>

[<span data-ttu-id="8bd0e-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="8bd0e-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="8bd0e-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="8bd0e-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="8bd0e-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="8bd0e-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

