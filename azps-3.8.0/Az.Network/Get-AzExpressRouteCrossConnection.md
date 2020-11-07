---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: a6a3b973a893e3588b5df77700318a725bde11b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959403"
---
# <span data-ttu-id="eb42e-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eb42e-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="eb42e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb42e-102">SYNOPSIS</span></span>
<span data-ttu-id="eb42e-103">從 Azure 取得 Azure ExpressRoute 交叉連線。</span><span class="sxs-lookup"><span data-stu-id="eb42e-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="eb42e-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb42e-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb42e-105">說明</span><span class="sxs-lookup"><span data-stu-id="eb42e-105">DESCRIPTION</span></span>
<span data-ttu-id="eb42e-106">**AzExpressRouteCrossConnection** Cmdlet 是用來從您的訂閱中取得 ExpressRoute 交叉連線物件。</span><span class="sxs-lookup"><span data-stu-id="eb42e-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="eb42e-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eb42e-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="eb42e-108">示例</span><span class="sxs-lookup"><span data-stu-id="eb42e-108">EXAMPLES</span></span>

### <span data-ttu-id="eb42e-109">範例1：取得 ExpressRoute 交叉連線</span><span class="sxs-lookup"><span data-stu-id="eb42e-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="eb42e-110">範例2：使用篩選器列出 ExpressRoute 交叉連線</span><span class="sxs-lookup"><span data-stu-id="eb42e-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="eb42e-111">這個 Cmdlet 會列出所有以「test」開頭的 ExpressRoute 交叉連接</span><span class="sxs-lookup"><span data-stu-id="eb42e-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="eb42e-112">參數</span><span class="sxs-lookup"><span data-stu-id="eb42e-112">PARAMETERS</span></span>

### <span data-ttu-id="eb42e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb42e-113">-DefaultProfile</span></span>
<span data-ttu-id="eb42e-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb42e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb42e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb42e-115">-Name</span></span>
<span data-ttu-id="eb42e-116">ExpressRoute 交叉連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb42e-116">The name of the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="eb42e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb42e-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb42e-118">包含 ExpressRoute 交叉連線的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="eb42e-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="eb42e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb42e-119">CommonParameters</span></span>
<span data-ttu-id="eb42e-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb42e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb42e-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eb42e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb42e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="eb42e-122">INPUTS</span></span>

### <span data-ttu-id="eb42e-123">所有</span><span class="sxs-lookup"><span data-stu-id="eb42e-123">None</span></span>
<span data-ttu-id="eb42e-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="eb42e-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb42e-125">輸出</span><span class="sxs-lookup"><span data-stu-id="eb42e-125">OUTPUTS</span></span>

### <span data-ttu-id="eb42e-126">PSExpressRouteCrossConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="eb42e-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="eb42e-127">筆記</span><span class="sxs-lookup"><span data-stu-id="eb42e-127">NOTES</span></span>

## <span data-ttu-id="eb42e-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb42e-128">RELATED LINKS</span></span>

[<span data-ttu-id="eb42e-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="eb42e-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)