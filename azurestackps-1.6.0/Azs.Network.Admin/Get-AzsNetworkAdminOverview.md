---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d3c564a004c006a9fd77c6fb5cef034b402b0b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623222"
---
# <span data-ttu-id="c4d95-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="c4d95-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="c4d95-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4d95-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d95-103">取得網路資源提供者狀態的概覽。</span><span class="sxs-lookup"><span data-stu-id="c4d95-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="c4d95-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4d95-104">SYNTAX</span></span>

```
Get-AzsNetworkAdminOverview [<CommonParameters>]
```

## <span data-ttu-id="c4d95-105">說明</span><span class="sxs-lookup"><span data-stu-id="c4d95-105">DESCRIPTION</span></span>
<span data-ttu-id="c4d95-106">取得網路資源提供者狀態的概覽。</span><span class="sxs-lookup"><span data-stu-id="c4d95-106">Get an overview of the state of the network resource provider.</span></span> <span data-ttu-id="c4d95-107">個別屬性提供資源使用狀況的詳細計數，以及依元件進行健康情況。</span><span class="sxs-lookup"><span data-stu-id="c4d95-107">Individual properties provide detailed counts of resource usage and health by component.</span></span>

## <span data-ttu-id="c4d95-108">示例</span><span class="sxs-lookup"><span data-stu-id="c4d95-108">EXAMPLES</span></span>

### <span data-ttu-id="c4d95-109">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4d95-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkAdminOverview
```

<span data-ttu-id="c4d95-110">取得網路系統管理員概覽。</span><span class="sxs-lookup"><span data-stu-id="c4d95-110">Get network admin overview.</span></span>

### <span data-ttu-id="c4d95-111">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c4d95-111">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
(Get-AzsNetworkAdminOverview).PublicIpAddressUsage
```

<span data-ttu-id="c4d95-112">取得公用 ip 位址使用量。</span><span class="sxs-lookup"><span data-stu-id="c4d95-112">Get public ip address usage.</span></span>

## <span data-ttu-id="c4d95-113">參數</span><span class="sxs-lookup"><span data-stu-id="c4d95-113">PARAMETERS</span></span>

### <span data-ttu-id="c4d95-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d95-114">CommonParameters</span></span>
<span data-ttu-id="c4d95-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4d95-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d95-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c4d95-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d95-117">輸入</span><span class="sxs-lookup"><span data-stu-id="c4d95-117">INPUTS</span></span>

## <span data-ttu-id="c4d95-118">輸出</span><span class="sxs-lookup"><span data-stu-id="c4d95-118">OUTPUTS</span></span>

### <span data-ttu-id="c4d95-119">AdminOverview 中的 AzureStack 的管理</span><span class="sxs-lookup"><span data-stu-id="c4d95-119">Microsoft.AzureStack.Management.Network.Admin.Models.AdminOverview</span></span>

## <span data-ttu-id="c4d95-120">筆記</span><span class="sxs-lookup"><span data-stu-id="c4d95-120">NOTES</span></span>

## <span data-ttu-id="c4d95-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4d95-121">RELATED LINKS</span></span>

