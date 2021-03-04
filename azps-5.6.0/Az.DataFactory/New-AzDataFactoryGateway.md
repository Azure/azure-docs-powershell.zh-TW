---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGateway.md
ms.openlocfilehash: 04026cf8cc01e1733c44821824ca4b0682b2b66d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907665"
---
# <span data-ttu-id="4f900-101">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4f900-101">New-AzDataFactoryGateway</span></span>

## <span data-ttu-id="4f900-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4f900-102">SYNOPSIS</span></span>
<span data-ttu-id="4f900-103">為 Azure Data Factory 建立閘道。</span><span class="sxs-lookup"><span data-stu-id="4f900-103">Creates a gateway for an Azure Data Factory.</span></span>

## <span data-ttu-id="4f900-104">語法</span><span class="sxs-lookup"><span data-stu-id="4f900-104">SYNTAX</span></span>

### <span data-ttu-id="4f900-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="4f900-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f900-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4f900-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f900-107">描述</span><span class="sxs-lookup"><span data-stu-id="4f900-107">DESCRIPTION</span></span>
<span data-ttu-id="4f900-108">**New-AzDataFactoryGateway** Cmdlet 在 Azure Data Factory 中建立閘道。</span><span class="sxs-lookup"><span data-stu-id="4f900-108">The **New-AzDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="4f900-109">例子</span><span class="sxs-lookup"><span data-stu-id="4f900-109">EXAMPLES</span></span>

### <span data-ttu-id="4f900-110">範例 1：建立閘道</span><span class="sxs-lookup"><span data-stu-id="4f900-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name              : ContosoGateway
Description       : my gateway
Version           : 
Status            : NeedRegistration
VersionStatus     : None
CreateTime        : 8/22/2014 1:40:34 AM
RegisterTime      : 
LastConnectTime   : 
ExpiryTime        : 
ProvisioningState : Succeeded
Key               : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="4f900-111">此命令在名為 ADF 的資源群組中名為 WikiADF 的資料工廠中，建立名為 ContosoGateway 的閘道。</span><span class="sxs-lookup"><span data-stu-id="4f900-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="4f900-112">參數</span><span class="sxs-lookup"><span data-stu-id="4f900-112">PARAMETERS</span></span>

### <span data-ttu-id="4f900-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4f900-113">-DataFactory</span></span>
<span data-ttu-id="4f900-114">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="4f900-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4f900-115">此 Cmdlet 會為此參數指定的資料工廠建立閘道。</span><span class="sxs-lookup"><span data-stu-id="4f900-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4f900-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4f900-116">-DataFactoryName</span></span>
<span data-ttu-id="4f900-117">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f900-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4f900-118">此 Cmdlet 會為此參數指定的資料工廠建立閘道。</span><span class="sxs-lookup"><span data-stu-id="4f900-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4f900-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f900-119">-DefaultProfile</span></span>
<span data-ttu-id="4f900-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4f900-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f900-121">-描述</span><span class="sxs-lookup"><span data-stu-id="4f900-121">-Description</span></span>
<span data-ttu-id="4f900-122">指定閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="4f900-122">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f900-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f900-123">-Name</span></span>
<span data-ttu-id="4f900-124">指定要建立之閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f900-124">Specifies the name of the gateway to create.</span></span>

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

### <span data-ttu-id="4f900-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f900-125">-ResourceGroupName</span></span>
<span data-ttu-id="4f900-126">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f900-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4f900-127">此 Cmdlet 會建立屬於此參數指定之群組的閘道。</span><span class="sxs-lookup"><span data-stu-id="4f900-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4f900-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f900-128">CommonParameters</span></span>
<span data-ttu-id="4f900-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4f900-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f900-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4f900-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f900-131">輸入</span><span class="sxs-lookup"><span data-stu-id="4f900-131">INPUTS</span></span>

### <span data-ttu-id="4f900-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4f900-132">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="4f900-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4f900-133">System.String</span></span>

## <span data-ttu-id="4f900-134">輸出</span><span class="sxs-lookup"><span data-stu-id="4f900-134">OUTPUTS</span></span>

### <span data-ttu-id="4f900-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4f900-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="4f900-136">筆記</span><span class="sxs-lookup"><span data-stu-id="4f900-136">NOTES</span></span>
* <span data-ttu-id="4f900-137">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="4f900-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4f900-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f900-138">RELATED LINKS</span></span>

[<span data-ttu-id="4f900-139">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4f900-139">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="4f900-140">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4f900-140">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


