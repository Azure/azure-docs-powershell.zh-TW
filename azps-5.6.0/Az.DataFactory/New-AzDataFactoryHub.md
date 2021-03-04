---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: 91e1bb556f2464f535e64a870b5491fceb9eac4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906738"
---
# <span data-ttu-id="0155a-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="0155a-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="0155a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0155a-102">SYNOPSIS</span></span>
<span data-ttu-id="0155a-103">建立 Azure Data Factory 的中樞。</span><span class="sxs-lookup"><span data-stu-id="0155a-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="0155a-104">語法</span><span class="sxs-lookup"><span data-stu-id="0155a-104">SYNTAX</span></span>

### <span data-ttu-id="0155a-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="0155a-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0155a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0155a-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0155a-107">描述</span><span class="sxs-lookup"><span data-stu-id="0155a-107">DESCRIPTION</span></span>
<span data-ttu-id="0155a-108">**New-AzDataFactoryHub** Cmdlet 會使用指定的檔案定義，在指定的 Azure 資源群組和指定的資料工廠中，為 Azure Data Factory 建立中樞。</span><span class="sxs-lookup"><span data-stu-id="0155a-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="0155a-109">建立中樞之後，您可以使用它來儲存及管理群組中的連結服務，也可以新增管線至中樞。</span><span class="sxs-lookup"><span data-stu-id="0155a-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="0155a-110">例子</span><span class="sxs-lookup"><span data-stu-id="0155a-110">EXAMPLES</span></span>

### <span data-ttu-id="0155a-111">範例 1：建立中樞</span><span class="sxs-lookup"><span data-stu-id="0155a-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="0155a-112">此命令在資源群組 ADFResourceGroup 和資料工廠中建立名為 ContosoDataHub 的中樞，名為 ADFDataFactory。</span><span class="sxs-lookup"><span data-stu-id="0155a-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="0155a-113">參數</span><span class="sxs-lookup"><span data-stu-id="0155a-113">PARAMETERS</span></span>

### <span data-ttu-id="0155a-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0155a-114">-DataFactory</span></span>
<span data-ttu-id="0155a-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="0155a-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="0155a-116">此 Cmdlet 會為此參數指定的資料工廠建立中樞。</span><span class="sxs-lookup"><span data-stu-id="0155a-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0155a-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0155a-117">-DataFactoryName</span></span>
<span data-ttu-id="0155a-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="0155a-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0155a-119">此 Cmdlet 會為此參數指定的資料工廠建立中樞。</span><span class="sxs-lookup"><span data-stu-id="0155a-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0155a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0155a-120">-DefaultProfile</span></span>
<span data-ttu-id="0155a-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0155a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0155a-122">-檔案</span><span class="sxs-lookup"><span data-stu-id="0155a-122">-File</span></span>
<span data-ttu-id="0155a-123">指定包含中樞描述之 JSON (JSON) 之 JavaScript 物件標記法的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="0155a-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0155a-124">-強制</span><span class="sxs-lookup"><span data-stu-id="0155a-124">-Force</span></span>
<span data-ttu-id="0155a-125">表示此 Cmdlet 會取代現有的中樞，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0155a-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0155a-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="0155a-126">-Name</span></span>
<span data-ttu-id="0155a-127">指定要建立之中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="0155a-127">Specifies the name of the hub to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0155a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0155a-128">-ResourceGroupName</span></span>
<span data-ttu-id="0155a-129">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0155a-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0155a-130">此 Cmdlet 會建立屬於此參數指定之群組的中樞。</span><span class="sxs-lookup"><span data-stu-id="0155a-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0155a-131">-確認</span><span class="sxs-lookup"><span data-stu-id="0155a-131">-Confirm</span></span>
<span data-ttu-id="0155a-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0155a-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0155a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0155a-133">-WhatIf</span></span>
<span data-ttu-id="0155a-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0155a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0155a-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0155a-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0155a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0155a-136">CommonParameters</span></span>
<span data-ttu-id="0155a-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0155a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0155a-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0155a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0155a-139">輸入</span><span class="sxs-lookup"><span data-stu-id="0155a-139">INPUTS</span></span>

### <span data-ttu-id="0155a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0155a-140">System.String</span></span>

### <span data-ttu-id="0155a-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0155a-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="0155a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="0155a-142">OUTPUTS</span></span>

### <span data-ttu-id="0155a-143">Microsoft.Azure.Commands.DataFactories.models.PSHub</span><span class="sxs-lookup"><span data-stu-id="0155a-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="0155a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="0155a-144">NOTES</span></span>
* <span data-ttu-id="0155a-145">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="0155a-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0155a-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="0155a-146">RELATED LINKS</span></span>

[<span data-ttu-id="0155a-147">Get-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="0155a-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="0155a-148">Remove-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="0155a-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


