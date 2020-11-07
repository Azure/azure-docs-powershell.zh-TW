---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: c15a8b57338a6c5e7c2f054e07a0d26d716627fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790142"
---
# <span data-ttu-id="c8e3a-101">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c8e3a-101">Get-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="c8e3a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="c8e3a-103">從 Azure 取得 Azure ExpressRoute 交叉連線。</span><span class="sxs-lookup"><span data-stu-id="c8e3a-103">Gets an Azure ExpressRoute cross connection from Azure.</span></span>

## <span data-ttu-id="c8e3a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8e3a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8e3a-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8e3a-105">DESCRIPTION</span></span>
<span data-ttu-id="c8e3a-106">**AzExpressRouteCrossConnection** Cmdlet 是用來從您的訂閱中取得 ExpressRoute 交叉連線物件。</span><span class="sxs-lookup"><span data-stu-id="c8e3a-106">The **Get-AzExpressRouteCrossConnection** cmdlet is used to retrieve an ExpressRoute cross connection object from your subscription.</span></span>
<span data-ttu-id="c8e3a-107">AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c8e3a-107">AzureRmExpressRouteCrossConnection</span></span>

## <span data-ttu-id="c8e3a-108">示例</span><span class="sxs-lookup"><span data-stu-id="c8e3a-108">EXAMPLES</span></span>

### <span data-ttu-id="c8e3a-109">範例1：取得 ExpressRoute 交叉連線</span><span class="sxs-lookup"><span data-stu-id="c8e3a-109">Example 1: Get the ExpressRoute cross connection</span></span>
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### <span data-ttu-id="c8e3a-110">範例2：使用篩選器列出 ExpressRoute 交叉連線</span><span class="sxs-lookup"><span data-stu-id="c8e3a-110">Example 2: List the ExpressRoute cross connections using a filter</span></span>
```
Get-AzExpressRouteCrossConnection -Name test*
```

<span data-ttu-id="c8e3a-111">這個 Cmdlet 會列出所有以「test」開頭的 ExpressRoute 交叉連接</span><span class="sxs-lookup"><span data-stu-id="c8e3a-111">This cmdlet will list all ExpressRoute cross connections that begin with "test"</span></span>

## <span data-ttu-id="c8e3a-112">參數</span><span class="sxs-lookup"><span data-stu-id="c8e3a-112">PARAMETERS</span></span>

### <span data-ttu-id="c8e3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8e3a-113">-DefaultProfile</span></span>
<span data-ttu-id="c8e3a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8e3a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8e3a-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8e3a-115">-Name</span></span>
<span data-ttu-id="c8e3a-116">ExpressRoute 交叉連線的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8e3a-116">The name of the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="c8e3a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8e3a-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8e3a-118">包含 ExpressRoute 交叉連線的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c8e3a-118">The name of the resource group that contains the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="c8e3a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8e3a-119">CommonParameters</span></span>
<span data-ttu-id="c8e3a-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8e3a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8e3a-121">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c8e3a-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8e3a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c8e3a-122">INPUTS</span></span>

### <span data-ttu-id="c8e3a-123">所有</span><span class="sxs-lookup"><span data-stu-id="c8e3a-123">None</span></span>
<span data-ttu-id="c8e3a-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c8e3a-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8e3a-125">輸出</span><span class="sxs-lookup"><span data-stu-id="c8e3a-125">OUTPUTS</span></span>

### <span data-ttu-id="c8e3a-126">PSExpressRouteCrossConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c8e3a-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="c8e3a-127">筆記</span><span class="sxs-lookup"><span data-stu-id="c8e3a-127">NOTES</span></span>

## <span data-ttu-id="c8e3a-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8e3a-128">RELATED LINKS</span></span>

[<span data-ttu-id="c8e3a-129">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c8e3a-129">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)