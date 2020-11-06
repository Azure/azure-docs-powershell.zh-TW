---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: ca03b95748203546fb8d9235cb7822a4dde359a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455712"
---
# <span data-ttu-id="5d17a-101">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="5d17a-101">New-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="5d17a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d17a-102">SYNOPSIS</span></span>
<span data-ttu-id="5d17a-103">針對後端 HTTP 設定建立新的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="5d17a-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d17a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d17a-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d17a-105">說明</span><span class="sxs-lookup"><span data-stu-id="5d17a-105">DESCRIPTION</span></span>
<span data-ttu-id="5d17a-106">**新的-AzureRmApplicationGatewayConnectionDraining** Cmdlet 會為後端 HTTP 設定建立新的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="5d17a-106">The **New-AzureRmApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="5d17a-107">示例</span><span class="sxs-lookup"><span data-stu-id="5d17a-107">EXAMPLES</span></span>

### <span data-ttu-id="5d17a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="5d17a-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzureRmApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="5d17a-109">此命令會建立新的連接排出設定，並將 [Enabled] 設定為 True 並將 DrainTimeoutInSec 設定為42秒，並將其儲存在 $connectionDraining 中。</span><span class="sxs-lookup"><span data-stu-id="5d17a-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="5d17a-110">參數</span><span class="sxs-lookup"><span data-stu-id="5d17a-110">PARAMETERS</span></span>

### <span data-ttu-id="5d17a-111">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="5d17a-111">-DrainTimeoutInSec</span></span>
<span data-ttu-id="5d17a-112">連接排出作用中的秒數。</span><span class="sxs-lookup"><span data-stu-id="5d17a-112">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="5d17a-113">可接受的值為從1秒到3600秒。</span><span class="sxs-lookup"><span data-stu-id="5d17a-113">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="5d17a-114">-啟用</span><span class="sxs-lookup"><span data-stu-id="5d17a-114">-Enabled</span></span>
<span data-ttu-id="5d17a-115">是否已啟用連接排出功能。</span><span class="sxs-lookup"><span data-stu-id="5d17a-115">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="5d17a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d17a-116">-DefaultProfile</span></span>
<span data-ttu-id="5d17a-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5d17a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d17a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d17a-118">CommonParameters</span></span>
<span data-ttu-id="5d17a-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d17a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d17a-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5d17a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d17a-121">輸入</span><span class="sxs-lookup"><span data-stu-id="5d17a-121">INPUTS</span></span>

### <span data-ttu-id="5d17a-122">所有</span><span class="sxs-lookup"><span data-stu-id="5d17a-122">None</span></span>

## <span data-ttu-id="5d17a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="5d17a-123">OUTPUTS</span></span>

### <span data-ttu-id="5d17a-124">PSApplicationGatewayConnectionDraining 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5d17a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="5d17a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="5d17a-125">NOTES</span></span>

## <span data-ttu-id="5d17a-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d17a-126">RELATED LINKS</span></span>

[<span data-ttu-id="5d17a-127">AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="5d17a-127">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="5d17a-128">移除-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="5d17a-128">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="5d17a-129">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="5d17a-129">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

