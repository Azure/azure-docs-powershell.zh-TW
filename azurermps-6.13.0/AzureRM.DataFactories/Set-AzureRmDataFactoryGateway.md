---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactoryGateway.md
ms.openlocfilehash: c40999dfa9f1300502e8909a32eaf13a34d0bae0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451287"
---
# <span data-ttu-id="aff12-101">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="aff12-101">Set-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="aff12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aff12-102">SYNOPSIS</span></span>
<span data-ttu-id="aff12-103">設定 Azure 資料工廠中閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="aff12-103">Sets the description for a gateway in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aff12-104">句法</span><span class="sxs-lookup"><span data-stu-id="aff12-104">SYNTAX</span></span>

### <span data-ttu-id="aff12-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="aff12-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aff12-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="aff12-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aff12-107">說明</span><span class="sxs-lookup"><span data-stu-id="aff12-107">DESCRIPTION</span></span>
<span data-ttu-id="aff12-108">**AzureRmDataFactoryGateway** Cmdlet 會在 Azure 資料工廠中設定指定閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="aff12-108">The **Set-AzureRmDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="aff12-109">示例</span><span class="sxs-lookup"><span data-stu-id="aff12-109">EXAMPLES</span></span>

### <span data-ttu-id="aff12-110">範例1：設定閘道的描述</span><span class="sxs-lookup"><span data-stu-id="aff12-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name            : ContosoGateway
Description     : my gateway
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:31:09 AM
RegisterTime    : 8/22/2014 1:31:37 AM
LastConnectTime : 8/22/2014 1:41:41 AM
ExpiryTime      :
```

<span data-ttu-id="aff12-111">這個命令會在名為 WikiADF 的資料工廠中設定名為 ContosoGateway 的閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="aff12-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="aff12-112">Description 參數會指定新的描述。</span><span class="sxs-lookup"><span data-stu-id="aff12-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="aff12-113">參數</span><span class="sxs-lookup"><span data-stu-id="aff12-113">PARAMETERS</span></span>

### <span data-ttu-id="aff12-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="aff12-114">-DataFactory</span></span>
<span data-ttu-id="aff12-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="aff12-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="aff12-116">這個 Cmdlet 會設定此參數指定之資料工廠中閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="aff12-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="aff12-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="aff12-117">-DataFactoryName</span></span>
<span data-ttu-id="aff12-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="aff12-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="aff12-119">這個 Cmdlet 會設定此參數指定之資料工廠中閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="aff12-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="aff12-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff12-120">-DefaultProfile</span></span>
<span data-ttu-id="aff12-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="aff12-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aff12-122">-描述</span><span class="sxs-lookup"><span data-stu-id="aff12-122">-Description</span></span>
<span data-ttu-id="aff12-123">指定閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="aff12-123">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="aff12-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="aff12-124">-Name</span></span>
<span data-ttu-id="aff12-125">指定要設定描述的閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="aff12-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="aff12-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aff12-126">-ResourceGroupName</span></span>
<span data-ttu-id="aff12-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aff12-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="aff12-128">這個 Cmdlet 會設定屬於此參數指定之群組之閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="aff12-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="aff12-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff12-129">CommonParameters</span></span>
<span data-ttu-id="aff12-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aff12-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff12-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aff12-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff12-132">輸入</span><span class="sxs-lookup"><span data-stu-id="aff12-132">INPUTS</span></span>

### <span data-ttu-id="aff12-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="aff12-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="aff12-134">System.object</span><span class="sxs-lookup"><span data-stu-id="aff12-134">System.String</span></span>

## <span data-ttu-id="aff12-135">輸出</span><span class="sxs-lookup"><span data-stu-id="aff12-135">OUTPUTS</span></span>

### <span data-ttu-id="aff12-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="aff12-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="aff12-137">筆記</span><span class="sxs-lookup"><span data-stu-id="aff12-137">NOTES</span></span>
* <span data-ttu-id="aff12-138">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="aff12-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="aff12-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="aff12-139">RELATED LINKS</span></span>

[<span data-ttu-id="aff12-140">AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="aff12-140">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="aff12-141">新-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="aff12-141">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="aff12-142">移除-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="aff12-142">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)


