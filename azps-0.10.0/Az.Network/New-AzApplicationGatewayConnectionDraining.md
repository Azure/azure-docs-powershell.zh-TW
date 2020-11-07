---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 813569705831dcd3d8c379b3c40078184498899e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794322"
---
# <span data-ttu-id="bafa7-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="bafa7-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="bafa7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bafa7-102">SYNOPSIS</span></span>
<span data-ttu-id="bafa7-103">針對後端 HTTP 設定建立新的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="bafa7-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="bafa7-104">句法</span><span class="sxs-lookup"><span data-stu-id="bafa7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bafa7-105">說明</span><span class="sxs-lookup"><span data-stu-id="bafa7-105">DESCRIPTION</span></span>
<span data-ttu-id="bafa7-106">**新的-AzApplicationGatewayConnectionDraining** Cmdlet 會為後端 HTTP 設定建立新的連接排出配置。</span><span class="sxs-lookup"><span data-stu-id="bafa7-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="bafa7-107">示例</span><span class="sxs-lookup"><span data-stu-id="bafa7-107">EXAMPLES</span></span>

### <span data-ttu-id="bafa7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bafa7-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="bafa7-109">此命令會建立新的連接排出設定，並將 [Enabled] 設定為 True 並將 DrainTimeoutInSec 設定為42秒，並將其儲存在 $connectionDraining 中。</span><span class="sxs-lookup"><span data-stu-id="bafa7-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="bafa7-110">參數</span><span class="sxs-lookup"><span data-stu-id="bafa7-110">PARAMETERS</span></span>

### <span data-ttu-id="bafa7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bafa7-111">-DefaultProfile</span></span>
<span data-ttu-id="bafa7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bafa7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafa7-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="bafa7-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="bafa7-114">連接排出作用中的秒數。</span><span class="sxs-lookup"><span data-stu-id="bafa7-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="bafa7-115">可接受的值為從1秒到3600秒。</span><span class="sxs-lookup"><span data-stu-id="bafa7-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafa7-116">-啟用</span><span class="sxs-lookup"><span data-stu-id="bafa7-116">-Enabled</span></span>
<span data-ttu-id="bafa7-117">是否已啟用連接排出功能。</span><span class="sxs-lookup"><span data-stu-id="bafa7-117">Whether connection draining is enabled or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafa7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafa7-118">CommonParameters</span></span>
<span data-ttu-id="bafa7-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bafa7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafa7-120">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bafa7-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafa7-121">輸入</span><span class="sxs-lookup"><span data-stu-id="bafa7-121">INPUTS</span></span>

### <span data-ttu-id="bafa7-122">所有</span><span class="sxs-lookup"><span data-stu-id="bafa7-122">None</span></span>

## <span data-ttu-id="bafa7-123">輸出</span><span class="sxs-lookup"><span data-stu-id="bafa7-123">OUTPUTS</span></span>

### <span data-ttu-id="bafa7-124">PSApplicationGatewayConnectionDraining 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bafa7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="bafa7-125">筆記</span><span class="sxs-lookup"><span data-stu-id="bafa7-125">NOTES</span></span>

## <span data-ttu-id="bafa7-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="bafa7-126">RELATED LINKS</span></span>

[<span data-ttu-id="bafa7-127">AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="bafa7-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="bafa7-128">移除-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="bafa7-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="bafa7-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="bafa7-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

