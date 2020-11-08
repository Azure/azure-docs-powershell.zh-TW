---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B07FE1A2-732D-4CCF-A0DF-3CF6B91FB3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryHub.md
ms.openlocfilehash: 292a288850371a834f938143cf2ec4380504091b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965706"
---
# <span data-ttu-id="2f634-101">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="2f634-101">Get-AzDataFactoryHub</span></span>

## <span data-ttu-id="2f634-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f634-102">SYNOPSIS</span></span>
<span data-ttu-id="2f634-103">取得有關 Azure 資料工廠中的集線器的資訊。</span><span class="sxs-lookup"><span data-stu-id="2f634-103">Gets information about hubs in Azure Data Factory.</span></span>

## <span data-ttu-id="2f634-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f634-104">SYNTAX</span></span>

### <span data-ttu-id="2f634-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="2f634-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactoryName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f634-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="2f634-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryHub [[-Name] <String>] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f634-107">說明</span><span class="sxs-lookup"><span data-stu-id="2f634-107">DESCRIPTION</span></span>
<span data-ttu-id="2f634-108">**AzDataFactoryHub** Cmdlet 會取得 Azure 資料工廠中集線器的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f634-108">The **Get-AzDataFactoryHub** cmdlet gets information about hubs in Azure Data Factory.</span></span>
<span data-ttu-id="2f634-109">如果您指定中樞的名稱，此 Cmdlet 會取得該中樞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f634-109">If you specify the name of a hub, this cmdlet gets information about that hub.</span></span>
<span data-ttu-id="2f634-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠中所有中心的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f634-110">If you do not specify a name, this cmdlet gets information about all of the hubs in a data factory.</span></span>

## <span data-ttu-id="2f634-111">示例</span><span class="sxs-lookup"><span data-stu-id="2f634-111">EXAMPLES</span></span>

### <span data-ttu-id="2f634-112">範例1：取得所有資料中心</span><span class="sxs-lookup"><span data-stu-id="2f634-112">Example 1: Get all data hubs</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory"
```

<span data-ttu-id="2f634-113">這個命令會取得名為 ADFResourceGroup 的 Azure 資源群組中的所有資料中心，以及名為 ADFDataFactory 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="2f634-113">This command gets all data hubs in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

### <span data-ttu-id="2f634-114">範例2：取得特定資料中心</span><span class="sxs-lookup"><span data-stu-id="2f634-114">Example 2: Get a specific data hub</span></span>
```
PS C:\>Get-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "MyDataHub"
```

<span data-ttu-id="2f634-115">這個命令會取得名為 ADFResourceGroup 的 Azure 資源群組中名為 MyDataHub 的中心，以及名為 ADFDataFactory 的資料工廠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f634-115">This command gets information about the hub named MyDataHub in the Azure resource group named ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="2f634-116">參數</span><span class="sxs-lookup"><span data-stu-id="2f634-116">PARAMETERS</span></span>

### <span data-ttu-id="2f634-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="2f634-117">-DataFactory</span></span>
<span data-ttu-id="2f634-118">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="2f634-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="2f634-119">這個 Cmdlet 會取得此參數指定之資料工廠中之中樞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f634-119">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f634-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2f634-120">-DataFactoryName</span></span>
<span data-ttu-id="2f634-121">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f634-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="2f634-122">這個 Cmdlet 會取得此參數指定之資料工廠中之中樞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f634-122">This cmdlet gets information about hubs in the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f634-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f634-123">-DefaultProfile</span></span>
<span data-ttu-id="2f634-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2f634-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f634-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f634-125">-Name</span></span>
<span data-ttu-id="2f634-126">指定要取得資訊之中心的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f634-126">Specifies the name of the hub about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f634-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f634-127">-ResourceGroupName</span></span>
<span data-ttu-id="2f634-128">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f634-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="2f634-129">這個 Cmdlet 會取得屬於此參數指定之群組之中樞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f634-129">This cmdlet gets information about hubs that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f634-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f634-130">CommonParameters</span></span>
<span data-ttu-id="2f634-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f634-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f634-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2f634-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f634-133">輸入</span><span class="sxs-lookup"><span data-stu-id="2f634-133">INPUTS</span></span>

### <span data-ttu-id="2f634-134">System.object</span><span class="sxs-lookup"><span data-stu-id="2f634-134">System.String</span></span>

### <span data-ttu-id="2f634-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2f634-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="2f634-136">輸出</span><span class="sxs-lookup"><span data-stu-id="2f634-136">OUTPUTS</span></span>

### <span data-ttu-id="2f634-137">PSHub 中的 DataFactories。</span><span class="sxs-lookup"><span data-stu-id="2f634-137">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="2f634-138">筆記</span><span class="sxs-lookup"><span data-stu-id="2f634-138">NOTES</span></span>
* <span data-ttu-id="2f634-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="2f634-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2f634-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f634-140">RELATED LINKS</span></span>

[<span data-ttu-id="2f634-141">新-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="2f634-141">New-AzDataFactoryHub</span></span>](./New-AzDataFactoryHub.md)

[<span data-ttu-id="2f634-142">移除-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="2f634-142">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)

