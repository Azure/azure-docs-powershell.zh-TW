---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5f2769987c87942af78bda238de00df94168249a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449955"
---
# <span data-ttu-id="9c7ca-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9c7ca-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="9c7ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="9c7ca-103">取得資源群組中的 Azure 可用性集合。</span><span class="sxs-lookup"><span data-stu-id="9c7ca-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c7ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c7ca-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="9c7ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="9c7ca-105">DESCRIPTION</span></span>
<span data-ttu-id="9c7ca-106">**AzureRmAvailabilitySet** Cmdlet 可在資源群組中取得 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="9c7ca-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="9c7ca-107">您可以指定要取得的特定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c7ca-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="9c7ca-108">示例</span><span class="sxs-lookup"><span data-stu-id="9c7ca-108">EXAMPLES</span></span>

### <span data-ttu-id="9c7ca-109">範例1：取得特定的可用性集</span><span class="sxs-lookup"><span data-stu-id="9c7ca-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="9c7ca-110">這個命令會在名為 ResourceGroup11 的資源群組中取得名為 AvailablitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="9c7ca-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="9c7ca-111">範例2：取得所有的可用性集</span><span class="sxs-lookup"><span data-stu-id="9c7ca-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="9c7ca-112">這個命令會在名為 ResourceGroup11 的資源群組中取得所有的可用性集。</span><span class="sxs-lookup"><span data-stu-id="9c7ca-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="9c7ca-113">參數</span><span class="sxs-lookup"><span data-stu-id="9c7ca-113">PARAMETERS</span></span>

### <span data-ttu-id="9c7ca-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c7ca-114">-Name</span></span>
<span data-ttu-id="9c7ca-115">指定此 Cmdlet 所取得之可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c7ca-115">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ca-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c7ca-116">-ResourceGroupName</span></span>
<span data-ttu-id="9c7ca-117">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c7ca-117">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c7ca-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c7ca-118">CommonParameters</span></span>
<span data-ttu-id="9c7ca-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c7ca-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c7ca-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9c7ca-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c7ca-121">輸入</span><span class="sxs-lookup"><span data-stu-id="9c7ca-121">INPUTS</span></span>

### <span data-ttu-id="9c7ca-122">所有</span><span class="sxs-lookup"><span data-stu-id="9c7ca-122">None</span></span>
<span data-ttu-id="9c7ca-123">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9c7ca-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c7ca-124">輸出</span><span class="sxs-lookup"><span data-stu-id="9c7ca-124">OUTPUTS</span></span>

## <span data-ttu-id="9c7ca-125">筆記</span><span class="sxs-lookup"><span data-stu-id="9c7ca-125">NOTES</span></span>

## <span data-ttu-id="9c7ca-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c7ca-126">RELATED LINKS</span></span>

[<span data-ttu-id="9c7ca-127">新-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9c7ca-127">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="9c7ca-128">移除-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="9c7ca-128">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


