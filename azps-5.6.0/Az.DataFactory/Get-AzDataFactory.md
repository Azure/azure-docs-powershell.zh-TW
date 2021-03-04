---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: ff47851c998cb88bec7106e8aba6d47d16069321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908213"
---
# <span data-ttu-id="fa42d-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="fa42d-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="fa42d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fa42d-102">SYNOPSIS</span></span>
<span data-ttu-id="fa42d-103">進一瞭解更多資訊。</span><span class="sxs-lookup"><span data-stu-id="fa42d-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="fa42d-104">語法</span><span class="sxs-lookup"><span data-stu-id="fa42d-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa42d-105">描述</span><span class="sxs-lookup"><span data-stu-id="fa42d-105">DESCRIPTION</span></span>
<span data-ttu-id="fa42d-106">**Get-AzDataFactory** Cmdlet 會取得 Azure 資源群組中資料需求的資訊。</span><span class="sxs-lookup"><span data-stu-id="fa42d-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="fa42d-107">如果您指定資料工廠的名稱，此 Cmdlet 會獲得該資料工廠的資訊。</span><span class="sxs-lookup"><span data-stu-id="fa42d-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="fa42d-108">如果您未指定名稱，此 Cmdlet 會獲得 Azure 資源群組中所有資料工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="fa42d-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="fa42d-109">例子</span><span class="sxs-lookup"><span data-stu-id="fa42d-109">EXAMPLES</span></span>

### <span data-ttu-id="fa42d-110">範例 1：取得所有資料</span><span class="sxs-lookup"><span data-stu-id="fa42d-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzDataFactory -ResourceGroupName "ADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration

DataFactoryName   : WikiADF2
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="fa42d-111">此命令會顯示 Azure 訂閱中所有資料預訂的資訊。</span><span class="sxs-lookup"><span data-stu-id="fa42d-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="fa42d-112">範例 2：取得特定的資料工廠</span><span class="sxs-lookup"><span data-stu-id="fa42d-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="fa42d-113">此命令會在名為 ADF 的資源群組訂閱中顯示名為 WikiADF 的資料工廠相關資訊，然後將它儲存在 $DataFactory 變數中。</span><span class="sxs-lookup"><span data-stu-id="fa42d-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="fa42d-114">在後續 *的 Cmdlet* 中指定 DataFactory 參數，以使用儲存在 $DataFactory。</span><span class="sxs-lookup"><span data-stu-id="fa42d-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="fa42d-115">參數</span><span class="sxs-lookup"><span data-stu-id="fa42d-115">PARAMETERS</span></span>

### <span data-ttu-id="fa42d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa42d-116">-DefaultProfile</span></span>
<span data-ttu-id="fa42d-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="fa42d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa42d-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="fa42d-118">-Name</span></span>
<span data-ttu-id="fa42d-119">指定要取得資訊的資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="fa42d-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa42d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa42d-120">-ResourceGroupName</span></span>
<span data-ttu-id="fa42d-121">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa42d-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fa42d-122">此 Cmdlet 會獲得屬於此參數指定之群組之資料轉場的資訊。</span><span class="sxs-lookup"><span data-stu-id="fa42d-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa42d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa42d-123">CommonParameters</span></span>
<span data-ttu-id="fa42d-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fa42d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa42d-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="fa42d-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa42d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="fa42d-126">INPUTS</span></span>

### <span data-ttu-id="fa42d-127">System.String</span><span class="sxs-lookup"><span data-stu-id="fa42d-127">System.String</span></span>

## <span data-ttu-id="fa42d-128">輸出</span><span class="sxs-lookup"><span data-stu-id="fa42d-128">OUTPUTS</span></span>

### <span data-ttu-id="fa42d-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fa42d-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="fa42d-130">筆記</span><span class="sxs-lookup"><span data-stu-id="fa42d-130">NOTES</span></span>
* <span data-ttu-id="fa42d-131">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="fa42d-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fa42d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa42d-132">RELATED LINKS</span></span>

[<span data-ttu-id="fa42d-133">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="fa42d-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="fa42d-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="fa42d-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


