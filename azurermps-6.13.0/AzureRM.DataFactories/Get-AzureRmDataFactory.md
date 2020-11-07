---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactory.md
ms.openlocfilehash: cfe19786e0d40915fc9cac67561b7e99b5dac38e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626115"
---
# <span data-ttu-id="14ff8-101">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="14ff8-101">Get-AzureRmDataFactory</span></span>

## <span data-ttu-id="14ff8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="14ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="14ff8-103">取得資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="14ff8-103">Gets information about Data Factories.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14ff8-104">句法</span><span class="sxs-lookup"><span data-stu-id="14ff8-104">SYNTAX</span></span>

```
Get-AzureRmDataFactory [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14ff8-105">說明</span><span class="sxs-lookup"><span data-stu-id="14ff8-105">DESCRIPTION</span></span>
<span data-ttu-id="14ff8-106">**AzureRmDataFactory** Cmdlet 會取得 Azure 資源群組中資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="14ff8-106">The **Get-AzureRmDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="14ff8-107">如果您指定資料工廠的名稱，此 Cmdlet 會取得該資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="14ff8-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="14ff8-108">如果您沒有指定名稱，此 Cmdlet 會取得 Azure 資源群組中所有資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="14ff8-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="14ff8-109">示例</span><span class="sxs-lookup"><span data-stu-id="14ff8-109">EXAMPLES</span></span>

### <span data-ttu-id="14ff8-110">範例1：取得所有資料工廠</span><span class="sxs-lookup"><span data-stu-id="14ff8-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzureRmDataFactory -ResourceGroupName "ADF"
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

<span data-ttu-id="14ff8-111">這個命令會顯示有關 Azure 訂閱中所有資料工廠的資訊。</span><span class="sxs-lookup"><span data-stu-id="14ff8-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="14ff8-112">範例2：取得特定的資料工廠</span><span class="sxs-lookup"><span data-stu-id="14ff8-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="14ff8-113">這個命令會在名為「ADF」的資源群組的訂閱中，顯示名為 WikiADF 的資料工廠相關資訊，然後將它儲存在 $DataFactory 變數中。</span><span class="sxs-lookup"><span data-stu-id="14ff8-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="14ff8-114">在後續的 Cmdlet 中指定 *DataFactory* 參數，以使用 $DataFactory 中儲存的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="14ff8-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="14ff8-115">參數</span><span class="sxs-lookup"><span data-stu-id="14ff8-115">PARAMETERS</span></span>

### <span data-ttu-id="14ff8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ff8-116">-DefaultProfile</span></span>
<span data-ttu-id="14ff8-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="14ff8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14ff8-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="14ff8-118">-Name</span></span>
<span data-ttu-id="14ff8-119">指定要取得資訊之資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="14ff8-119">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="14ff8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14ff8-120">-ResourceGroupName</span></span>
<span data-ttu-id="14ff8-121">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="14ff8-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="14ff8-122">這個 Cmdlet 會取得屬於此參數指定之群組之資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="14ff8-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="14ff8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ff8-123">CommonParameters</span></span>
<span data-ttu-id="14ff8-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="14ff8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ff8-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="14ff8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ff8-126">輸入</span><span class="sxs-lookup"><span data-stu-id="14ff8-126">INPUTS</span></span>

### <span data-ttu-id="14ff8-127">System.object</span><span class="sxs-lookup"><span data-stu-id="14ff8-127">System.String</span></span>

## <span data-ttu-id="14ff8-128">輸出</span><span class="sxs-lookup"><span data-stu-id="14ff8-128">OUTPUTS</span></span>

### <span data-ttu-id="14ff8-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="14ff8-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="14ff8-130">筆記</span><span class="sxs-lookup"><span data-stu-id="14ff8-130">NOTES</span></span>
* <span data-ttu-id="14ff8-131">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="14ff8-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="14ff8-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="14ff8-132">RELATED LINKS</span></span>

[<span data-ttu-id="14ff8-133">新-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="14ff8-133">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)

[<span data-ttu-id="14ff8-134">移除-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="14ff8-134">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


