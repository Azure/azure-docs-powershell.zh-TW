---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 0b7d1f72b25da91e85a578a88eded7a511d6d1fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913362"
---
# <span data-ttu-id="4385f-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="4385f-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="4385f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4385f-102">SYNOPSIS</span></span>
<span data-ttu-id="4385f-103">測試 PowerBI 內嵌容量實例是否存在。</span><span class="sxs-lookup"><span data-stu-id="4385f-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="4385f-104">語法</span><span class="sxs-lookup"><span data-stu-id="4385f-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4385f-105">描述</span><span class="sxs-lookup"><span data-stu-id="4385f-105">DESCRIPTION</span></span>
<span data-ttu-id="4385f-106">此Test-AzPowerBIEmbeddedCapacity Cmdlet 會測試 PowerBI 內嵌容量實例是否存在</span><span class="sxs-lookup"><span data-stu-id="4385f-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="4385f-107">例子</span><span class="sxs-lookup"><span data-stu-id="4385f-107">EXAMPLES</span></span>

### <span data-ttu-id="4385f-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4385f-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="4385f-109">此命令會測試是否有名為 test搶取的容量</span><span class="sxs-lookup"><span data-stu-id="4385f-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="4385f-110">參數</span><span class="sxs-lookup"><span data-stu-id="4385f-110">PARAMETERS</span></span>

### <span data-ttu-id="4385f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4385f-111">-DefaultProfile</span></span>
<span data-ttu-id="4385f-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4385f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4385f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="4385f-113">-Name</span></span>
<span data-ttu-id="4385f-114">PowerBI 內嵌容量的名稱</span><span class="sxs-lookup"><span data-stu-id="4385f-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="4385f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4385f-115">CommonParameters</span></span>
<span data-ttu-id="4385f-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4385f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4385f-117">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4385f-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4385f-118">輸入</span><span class="sxs-lookup"><span data-stu-id="4385f-118">INPUTS</span></span>

### <span data-ttu-id="4385f-119">沒有</span><span class="sxs-lookup"><span data-stu-id="4385f-119">None</span></span>

## <span data-ttu-id="4385f-120">輸出</span><span class="sxs-lookup"><span data-stu-id="4385f-120">OUTPUTS</span></span>

### <span data-ttu-id="4385f-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4385f-121">System.Boolean</span></span>

## <span data-ttu-id="4385f-122">筆記</span><span class="sxs-lookup"><span data-stu-id="4385f-122">NOTES</span></span>

## <span data-ttu-id="4385f-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="4385f-123">RELATED LINKS</span></span>

[<span data-ttu-id="4385f-124">Get-AzPowerBIEmbedded一切</span><span class="sxs-lookup"><span data-stu-id="4385f-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="4385f-125">Remove-AzPowerBIEmbedded一切</span><span class="sxs-lookup"><span data-stu-id="4385f-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
