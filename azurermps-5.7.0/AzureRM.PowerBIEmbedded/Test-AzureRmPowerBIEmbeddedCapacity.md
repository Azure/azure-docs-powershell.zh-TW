---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8f6e161ad9ae2078da15dda659f1aea13929eec9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444464"
---
# <span data-ttu-id="33c28-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="33c28-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="33c28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="33c28-102">SYNOPSIS</span></span>
<span data-ttu-id="33c28-103">測試 PowerBI 內嵌容量的實例是否存在。</span><span class="sxs-lookup"><span data-stu-id="33c28-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33c28-104">句法</span><span class="sxs-lookup"><span data-stu-id="33c28-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="33c28-105">說明</span><span class="sxs-lookup"><span data-stu-id="33c28-105">DESCRIPTION</span></span>
<span data-ttu-id="33c28-106">Test-AzureRmPowerBIEmbeddedCapacity Cmdlet 會測試 PowerBI 內嵌容量的實例是否存在</span><span class="sxs-lookup"><span data-stu-id="33c28-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="33c28-107">示例</span><span class="sxs-lookup"><span data-stu-id="33c28-107">EXAMPLES</span></span>

### <span data-ttu-id="33c28-108">範例1</span><span class="sxs-lookup"><span data-stu-id="33c28-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="33c28-109">這個命令會測試是否有名為 testcapacity 的容量。</span><span class="sxs-lookup"><span data-stu-id="33c28-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="33c28-110">參數</span><span class="sxs-lookup"><span data-stu-id="33c28-110">PARAMETERS</span></span>

### <span data-ttu-id="33c28-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="33c28-111">-Name</span></span>
<span data-ttu-id="33c28-112">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="33c28-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="33c28-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c28-113">CommonParameters</span></span>
<span data-ttu-id="33c28-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="33c28-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c28-115">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="33c28-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c28-116">輸入</span><span class="sxs-lookup"><span data-stu-id="33c28-116">INPUTS</span></span>

### <span data-ttu-id="33c28-117">所有</span><span class="sxs-lookup"><span data-stu-id="33c28-117">None</span></span>
<span data-ttu-id="33c28-118">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="33c28-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="33c28-119">輸出</span><span class="sxs-lookup"><span data-stu-id="33c28-119">OUTPUTS</span></span>

### <span data-ttu-id="33c28-120">System.object</span><span class="sxs-lookup"><span data-stu-id="33c28-120">System.Boolean</span></span>

## <span data-ttu-id="33c28-121">筆記</span><span class="sxs-lookup"><span data-stu-id="33c28-121">NOTES</span></span>

## <span data-ttu-id="33c28-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="33c28-122">RELATED LINKS</span></span>

[<span data-ttu-id="33c28-123">AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="33c28-123">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="33c28-124">移除-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="33c28-124">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
