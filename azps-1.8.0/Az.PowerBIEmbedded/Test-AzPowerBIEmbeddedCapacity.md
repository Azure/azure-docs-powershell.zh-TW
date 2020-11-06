---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 80fc102c31e4019576a6f2c65ee1c93e19b81590
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621247"
---
# <span data-ttu-id="68f53-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="68f53-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="68f53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68f53-102">SYNOPSIS</span></span>
<span data-ttu-id="68f53-103">測試 PowerBI 內嵌容量的實例是否存在。</span><span class="sxs-lookup"><span data-stu-id="68f53-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="68f53-104">句法</span><span class="sxs-lookup"><span data-stu-id="68f53-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68f53-105">說明</span><span class="sxs-lookup"><span data-stu-id="68f53-105">DESCRIPTION</span></span>
<span data-ttu-id="68f53-106">Test-AzPowerBIEmbeddedCapacity Cmdlet 會測試 PowerBI 內嵌容量的實例是否存在</span><span class="sxs-lookup"><span data-stu-id="68f53-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="68f53-107">示例</span><span class="sxs-lookup"><span data-stu-id="68f53-107">EXAMPLES</span></span>

### <span data-ttu-id="68f53-108">範例1</span><span class="sxs-lookup"><span data-stu-id="68f53-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="68f53-109">這個命令會測試是否有名為 testcapacity 的容量。</span><span class="sxs-lookup"><span data-stu-id="68f53-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="68f53-110">參數</span><span class="sxs-lookup"><span data-stu-id="68f53-110">PARAMETERS</span></span>

### <span data-ttu-id="68f53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68f53-111">-DefaultProfile</span></span>
<span data-ttu-id="68f53-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68f53-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68f53-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="68f53-113">-Name</span></span>
<span data-ttu-id="68f53-114">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="68f53-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68f53-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68f53-115">CommonParameters</span></span>
<span data-ttu-id="68f53-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68f53-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68f53-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="68f53-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68f53-118">輸入</span><span class="sxs-lookup"><span data-stu-id="68f53-118">INPUTS</span></span>

### <span data-ttu-id="68f53-119">所有</span><span class="sxs-lookup"><span data-stu-id="68f53-119">None</span></span>

## <span data-ttu-id="68f53-120">輸出</span><span class="sxs-lookup"><span data-stu-id="68f53-120">OUTPUTS</span></span>

### <span data-ttu-id="68f53-121">System.object</span><span class="sxs-lookup"><span data-stu-id="68f53-121">System.Boolean</span></span>

## <span data-ttu-id="68f53-122">筆記</span><span class="sxs-lookup"><span data-stu-id="68f53-122">NOTES</span></span>

## <span data-ttu-id="68f53-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="68f53-123">RELATED LINKS</span></span>

[<span data-ttu-id="68f53-124">AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="68f53-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="68f53-125">移除-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="68f53-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
