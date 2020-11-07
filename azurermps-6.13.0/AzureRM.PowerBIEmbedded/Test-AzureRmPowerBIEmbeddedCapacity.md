---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 306bb6e4e12adcb4a4eda65b2517ddf0648a81fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624356"
---
# <span data-ttu-id="b39db-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b39db-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="b39db-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b39db-102">SYNOPSIS</span></span>
<span data-ttu-id="b39db-103">測試 PowerBI 內嵌容量的實例是否存在。</span><span class="sxs-lookup"><span data-stu-id="b39db-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b39db-104">句法</span><span class="sxs-lookup"><span data-stu-id="b39db-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b39db-105">說明</span><span class="sxs-lookup"><span data-stu-id="b39db-105">DESCRIPTION</span></span>
<span data-ttu-id="b39db-106">Test-AzureRmPowerBIEmbeddedCapacity Cmdlet 會測試 PowerBI 內嵌容量的實例是否存在</span><span class="sxs-lookup"><span data-stu-id="b39db-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="b39db-107">示例</span><span class="sxs-lookup"><span data-stu-id="b39db-107">EXAMPLES</span></span>

### <span data-ttu-id="b39db-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b39db-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="b39db-109">這個命令會測試是否有名為 testcapacity 的容量。</span><span class="sxs-lookup"><span data-stu-id="b39db-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="b39db-110">參數</span><span class="sxs-lookup"><span data-stu-id="b39db-110">PARAMETERS</span></span>

### <span data-ttu-id="b39db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b39db-111">-DefaultProfile</span></span>
<span data-ttu-id="b39db-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b39db-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b39db-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b39db-113">-Name</span></span>
<span data-ttu-id="b39db-114">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="b39db-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="b39db-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b39db-115">CommonParameters</span></span>
<span data-ttu-id="b39db-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b39db-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b39db-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b39db-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b39db-118">輸入</span><span class="sxs-lookup"><span data-stu-id="b39db-118">INPUTS</span></span>

### <span data-ttu-id="b39db-119">所有</span><span class="sxs-lookup"><span data-stu-id="b39db-119">None</span></span>

## <span data-ttu-id="b39db-120">輸出</span><span class="sxs-lookup"><span data-stu-id="b39db-120">OUTPUTS</span></span>

### <span data-ttu-id="b39db-121">System.object</span><span class="sxs-lookup"><span data-stu-id="b39db-121">System.Boolean</span></span>

## <span data-ttu-id="b39db-122">筆記</span><span class="sxs-lookup"><span data-stu-id="b39db-122">NOTES</span></span>

## <span data-ttu-id="b39db-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="b39db-123">RELATED LINKS</span></span>

[<span data-ttu-id="b39db-124">AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b39db-124">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="b39db-125">移除-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="b39db-125">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
