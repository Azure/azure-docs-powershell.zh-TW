---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: B656B4C4-97DE-4F9F-937C-E115CB3F0E80
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryHub.md
ms.openlocfilehash: 1155b7c0b294ac3bc5c2106b473ce1cf55a9ac82
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285211"
---
# <span data-ttu-id="9d7e0-101">New-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="9d7e0-101">New-AzDataFactoryHub</span></span>

## <span data-ttu-id="9d7e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="9d7e0-103">為 Azure 資料工廠建立中樞。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-103">Creates a hub for an Azure Data Factory.</span></span>

## <span data-ttu-id="9d7e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d7e0-104">SYNTAX</span></span>

### <span data-ttu-id="9d7e0-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="9d7e0-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactoryName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d7e0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9d7e0-106">ByFactoryObject</span></span>
```
New-AzDataFactoryHub [-Name] <String> [-File] <String> [-Force] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d7e0-107">說明</span><span class="sxs-lookup"><span data-stu-id="9d7e0-107">DESCRIPTION</span></span>
<span data-ttu-id="9d7e0-108">**新的-AzDataFactoryHub** Cmdlet 會在指定的 azure 資源群組和指定的資料工廠中，以指定的檔案定義來建立一個中樞，以供 Azure 資料工廠使用。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-108">The **New-AzDataFactoryHub** cmdlet creates a hub for Azure Data Factory in the specified Azure resource group and in the specified data factory with the specified file definition.</span></span>
<span data-ttu-id="9d7e0-109">建立中樞之後，您可以使用它來儲存及管理群組中的連結服務，而且您可以在中樞中新增管線。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-109">After you create the hub, you can use it to store and manage linked services in a group, and you can add pipelines to the hub.</span></span>

## <span data-ttu-id="9d7e0-110">示例</span><span class="sxs-lookup"><span data-stu-id="9d7e0-110">EXAMPLES</span></span>

### <span data-ttu-id="9d7e0-111">範例1：建立中樞</span><span class="sxs-lookup"><span data-stu-id="9d7e0-111">Example 1: Create a hub</span></span>
```
PS C:\>New-AzDataFactoryHub -ResourceGroupName "ADFResourceGroup" -DataFactoryName "ADFDataFactory" -Name "ContosoDataHub" -File "C:\Hub.json"
```

<span data-ttu-id="9d7e0-112">這個命令會在資源群組 ADFResourceGroup 和名為 ADFDataFactory 的資料工廠中，建立名為 ContosoDataHub 的中樞。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-112">This command creates a hub named ContosoDataHub in the resource group ADFResourceGroup and the data factory named ADFDataFactory.</span></span>

## <span data-ttu-id="9d7e0-113">參數</span><span class="sxs-lookup"><span data-stu-id="9d7e0-113">PARAMETERS</span></span>

### <span data-ttu-id="9d7e0-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9d7e0-114">-DataFactory</span></span>
<span data-ttu-id="9d7e0-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9d7e0-116">這個 Cmdlet 會為此參數指定的資料工廠建立中樞。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-116">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d7e0-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9d7e0-117">-DataFactoryName</span></span>
<span data-ttu-id="9d7e0-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9d7e0-119">這個 Cmdlet 會為此參數指定的資料工廠建立中樞。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-119">This cmdlet creates a hub for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d7e0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d7e0-120">-DefaultProfile</span></span>
<span data-ttu-id="9d7e0-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9d7e0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d7e0-122">檔案</span><span class="sxs-lookup"><span data-stu-id="9d7e0-122">-File</span></span>
<span data-ttu-id="9d7e0-123">指定包含中樞說明的 JavaScript 物件符號 (JSON) 檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-123">Specifies the full path of the JavaScript Object Notation (JSON) file that contains the description of the hub.</span></span>

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

### <span data-ttu-id="9d7e0-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9d7e0-124">-Force</span></span>
<span data-ttu-id="9d7e0-125">表示此 Cmdlet 會取代現有的中樞，而不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-125">Indicates that this cmdlet replaces an existing hub without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="9d7e0-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="9d7e0-126">-Name</span></span>
<span data-ttu-id="9d7e0-127">指定要建立之中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-127">Specifies the name of the hub to create.</span></span>

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

### <span data-ttu-id="9d7e0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d7e0-128">-ResourceGroupName</span></span>
<span data-ttu-id="9d7e0-129">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9d7e0-130">這個 Cmdlet 會建立屬於此參數指定之群組的中樞。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-130">This cmdlet creates a hub that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9d7e0-131">-確認</span><span class="sxs-lookup"><span data-stu-id="9d7e0-131">-Confirm</span></span>
<span data-ttu-id="9d7e0-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d7e0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d7e0-133">-WhatIf</span></span>
<span data-ttu-id="9d7e0-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d7e0-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d7e0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d7e0-136">CommonParameters</span></span>
<span data-ttu-id="9d7e0-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d7e0-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d7e0-139">輸入</span><span class="sxs-lookup"><span data-stu-id="9d7e0-139">INPUTS</span></span>

### <span data-ttu-id="9d7e0-140">System.object</span><span class="sxs-lookup"><span data-stu-id="9d7e0-140">System.String</span></span>

### <span data-ttu-id="9d7e0-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9d7e0-141">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="9d7e0-142">輸出</span><span class="sxs-lookup"><span data-stu-id="9d7e0-142">OUTPUTS</span></span>

### <span data-ttu-id="9d7e0-143">PSHub 中的 DataFactories。</span><span class="sxs-lookup"><span data-stu-id="9d7e0-143">Microsoft.Azure.Commands.DataFactories.Models.PSHub</span></span>

## <span data-ttu-id="9d7e0-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9d7e0-144">NOTES</span></span>
* <span data-ttu-id="9d7e0-145">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="9d7e0-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9d7e0-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d7e0-146">RELATED LINKS</span></span>

[<span data-ttu-id="9d7e0-147">AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="9d7e0-147">Get-AzDataFactoryHub</span></span>](./Get-AzDataFactoryHub.md)

[<span data-ttu-id="9d7e0-148">移除-AzDataFactoryHub</span><span class="sxs-lookup"><span data-stu-id="9d7e0-148">Remove-AzDataFactoryHub</span></span>](./Remove-AzDataFactoryHub.md)


