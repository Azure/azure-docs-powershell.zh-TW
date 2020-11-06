---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 4DCF54BA-CFFA-4555-8CA3-66B98F704EFB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGateway.md
ms.openlocfilehash: 4b94c3e0d178748169b5faaa3b7eb43b76f8bc4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449906"
---
# <span data-ttu-id="546f2-101">New-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="546f2-101">New-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="546f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="546f2-102">SYNOPSIS</span></span>
<span data-ttu-id="546f2-103">建立 Azure 資料工廠的閘道。</span><span class="sxs-lookup"><span data-stu-id="546f2-103">Creates a gateway for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="546f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="546f2-104">SYNTAX</span></span>

### <span data-ttu-id="546f2-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="546f2-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [[-Description] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="546f2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="546f2-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [[-Description] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="546f2-107">說明</span><span class="sxs-lookup"><span data-stu-id="546f2-107">DESCRIPTION</span></span>
<span data-ttu-id="546f2-108">**新的-AzureRmDataFactoryGateway** Cmdlet 會在 Azure 資料工廠中建立閘道。</span><span class="sxs-lookup"><span data-stu-id="546f2-108">The **New-AzureRmDataFactoryGateway** cmdlet creates a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="546f2-109">示例</span><span class="sxs-lookup"><span data-stu-id="546f2-109">EXAMPLES</span></span>

### <span data-ttu-id="546f2-110">範例1：建立閘道</span><span class="sxs-lookup"><span data-stu-id="546f2-110">Example 1: Create a gateway</span></span>
```
PS C:\>New-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="546f2-111">這個命令會在名為 [ADF] 資源群組的資料工廠中，建立名為 ContosoGateway 的閘道。</span><span class="sxs-lookup"><span data-stu-id="546f2-111">This command creates a gateway named ContosoGateway in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="546f2-112">參數</span><span class="sxs-lookup"><span data-stu-id="546f2-112">PARAMETERS</span></span>

### <span data-ttu-id="546f2-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="546f2-113">-DataFactory</span></span>
<span data-ttu-id="546f2-114">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="546f2-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="546f2-115">這個 Cmdlet 會為此參數指定的資料工廠建立閘道。</span><span class="sxs-lookup"><span data-stu-id="546f2-115">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546f2-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="546f2-116">-DataFactoryName</span></span>
<span data-ttu-id="546f2-117">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="546f2-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="546f2-118">這個 Cmdlet 會為此參數指定的資料工廠建立閘道。</span><span class="sxs-lookup"><span data-stu-id="546f2-118">This cmdlet creates a gateway for the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546f2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="546f2-119">-DefaultProfile</span></span>
<span data-ttu-id="546f2-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="546f2-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="546f2-121">-描述</span><span class="sxs-lookup"><span data-stu-id="546f2-121">-Description</span></span>
<span data-ttu-id="546f2-122">指定閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="546f2-122">Specifies a description for the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546f2-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="546f2-123">-Name</span></span>
<span data-ttu-id="546f2-124">指定要建立之閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="546f2-124">Specifies the name of the gateway to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546f2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="546f2-125">-ResourceGroupName</span></span>
<span data-ttu-id="546f2-126">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="546f2-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="546f2-127">這個 Cmdlet 會建立屬於此參數指定之群組的閘道。</span><span class="sxs-lookup"><span data-stu-id="546f2-127">This cmdlet creates a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="546f2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="546f2-128">CommonParameters</span></span>
<span data-ttu-id="546f2-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="546f2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="546f2-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="546f2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="546f2-131">輸入</span><span class="sxs-lookup"><span data-stu-id="546f2-131">INPUTS</span></span>

### <span data-ttu-id="546f2-132">所有</span><span class="sxs-lookup"><span data-stu-id="546f2-132">None</span></span>
<span data-ttu-id="546f2-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="546f2-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="546f2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="546f2-134">OUTPUTS</span></span>

### <span data-ttu-id="546f2-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="546f2-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="546f2-136">筆記</span><span class="sxs-lookup"><span data-stu-id="546f2-136">NOTES</span></span>
* <span data-ttu-id="546f2-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="546f2-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="546f2-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="546f2-138">RELATED LINKS</span></span>

[<span data-ttu-id="546f2-139">移除-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="546f2-139">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="546f2-140">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="546f2-140">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


