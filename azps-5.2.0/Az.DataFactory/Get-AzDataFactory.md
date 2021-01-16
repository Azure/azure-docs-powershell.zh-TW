---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: 11aaaa3bb17a35583655f231123b7f6e9dea9ab4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280960"
---
# <span data-ttu-id="a9b58-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a9b58-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="a9b58-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9b58-102">SYNOPSIS</span></span>
<span data-ttu-id="a9b58-103">取得資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9b58-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="a9b58-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9b58-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9b58-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9b58-105">DESCRIPTION</span></span>
<span data-ttu-id="a9b58-106">**AzDataFactory** Cmdlet 會取得 Azure 資源群組中資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9b58-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="a9b58-107">如果您指定資料工廠的名稱，此 Cmdlet 會取得該資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9b58-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="a9b58-108">如果您沒有指定名稱，此 Cmdlet 會取得 Azure 資源群組中所有資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9b58-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="a9b58-109">示例</span><span class="sxs-lookup"><span data-stu-id="a9b58-109">EXAMPLES</span></span>

### <span data-ttu-id="a9b58-110">範例1：取得所有資料工廠</span><span class="sxs-lookup"><span data-stu-id="a9b58-110">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="a9b58-111">這個命令會顯示有關 Azure 訂閱中所有資料工廠的資訊。</span><span class="sxs-lookup"><span data-stu-id="a9b58-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="a9b58-112">範例2：取得特定的資料工廠</span><span class="sxs-lookup"><span data-stu-id="a9b58-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="a9b58-113">這個命令會在名為「ADF」的資源群組的訂閱中，顯示名為 WikiADF 的資料工廠相關資訊，然後將它儲存在 $DataFactory 變數中。</span><span class="sxs-lookup"><span data-stu-id="a9b58-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="a9b58-114">在後續的 Cmdlet 中指定 *DataFactory* 參數，以使用 $DataFactory 中儲存的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="a9b58-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="a9b58-115">參數</span><span class="sxs-lookup"><span data-stu-id="a9b58-115">PARAMETERS</span></span>

### <span data-ttu-id="a9b58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9b58-116">-DefaultProfile</span></span>
<span data-ttu-id="a9b58-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a9b58-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9b58-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9b58-118">-Name</span></span>
<span data-ttu-id="a9b58-119">指定要取得資訊之資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9b58-119">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="a9b58-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9b58-120">-ResourceGroupName</span></span>
<span data-ttu-id="a9b58-121">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9b58-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a9b58-122">這個 Cmdlet 會取得屬於此參數指定之群組之資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a9b58-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a9b58-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9b58-123">CommonParameters</span></span>
<span data-ttu-id="a9b58-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9b58-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9b58-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a9b58-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9b58-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a9b58-126">INPUTS</span></span>

### <span data-ttu-id="a9b58-127">System.object</span><span class="sxs-lookup"><span data-stu-id="a9b58-127">System.String</span></span>

## <span data-ttu-id="a9b58-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a9b58-128">OUTPUTS</span></span>

### <span data-ttu-id="a9b58-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a9b58-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="a9b58-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a9b58-130">NOTES</span></span>
* <span data-ttu-id="a9b58-131">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="a9b58-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a9b58-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9b58-132">RELATED LINKS</span></span>

[<span data-ttu-id="a9b58-133">新-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a9b58-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="a9b58-134">移除-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="a9b58-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


