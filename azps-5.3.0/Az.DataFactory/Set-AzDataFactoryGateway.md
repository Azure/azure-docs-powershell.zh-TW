---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: b9eebe26e64e9a7ce2497cdf9984ca6dabb062e0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98439439"
---
# <span data-ttu-id="c169b-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="c169b-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="c169b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c169b-102">SYNOPSIS</span></span>
<span data-ttu-id="c169b-103">設定 Azure 資料工廠中閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="c169b-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="c169b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c169b-104">SYNTAX</span></span>

### <span data-ttu-id="c169b-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="c169b-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c169b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c169b-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c169b-107">說明</span><span class="sxs-lookup"><span data-stu-id="c169b-107">DESCRIPTION</span></span>
<span data-ttu-id="c169b-108">**AzDataFactoryGateway** Cmdlet 會在 Azure 資料工廠中設定指定閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="c169b-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="c169b-109">示例</span><span class="sxs-lookup"><span data-stu-id="c169b-109">EXAMPLES</span></span>

### <span data-ttu-id="c169b-110">範例1：設定閘道的描述</span><span class="sxs-lookup"><span data-stu-id="c169b-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
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

<span data-ttu-id="c169b-111">這個命令會在名為 WikiADF 的資料工廠中設定名為 ContosoGateway 的閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="c169b-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="c169b-112">Description 參數會指定新的描述。</span><span class="sxs-lookup"><span data-stu-id="c169b-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="c169b-113">參數</span><span class="sxs-lookup"><span data-stu-id="c169b-113">PARAMETERS</span></span>

### <span data-ttu-id="c169b-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c169b-114">-DataFactory</span></span>
<span data-ttu-id="c169b-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="c169b-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c169b-116">這個 Cmdlet 會設定此參數指定之資料工廠中閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="c169b-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c169b-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c169b-117">-DataFactoryName</span></span>
<span data-ttu-id="c169b-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="c169b-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c169b-119">這個 Cmdlet 會設定此參數指定之資料工廠中閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="c169b-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c169b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c169b-120">-DefaultProfile</span></span>
<span data-ttu-id="c169b-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c169b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c169b-122">-描述</span><span class="sxs-lookup"><span data-stu-id="c169b-122">-Description</span></span>
<span data-ttu-id="c169b-123">指定閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="c169b-123">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="c169b-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="c169b-124">-Name</span></span>
<span data-ttu-id="c169b-125">指定要設定描述的閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="c169b-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="c169b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c169b-126">-ResourceGroupName</span></span>
<span data-ttu-id="c169b-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c169b-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c169b-128">這個 Cmdlet 會設定屬於此參數指定之群組之閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="c169b-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c169b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c169b-129">CommonParameters</span></span>
<span data-ttu-id="c169b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c169b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c169b-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c169b-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c169b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c169b-132">INPUTS</span></span>

### <span data-ttu-id="c169b-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c169b-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="c169b-134">System.object</span><span class="sxs-lookup"><span data-stu-id="c169b-134">System.String</span></span>

## <span data-ttu-id="c169b-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c169b-135">OUTPUTS</span></span>

### <span data-ttu-id="c169b-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="c169b-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="c169b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c169b-137">NOTES</span></span>
* <span data-ttu-id="c169b-138">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="c169b-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c169b-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c169b-139">RELATED LINKS</span></span>

[<span data-ttu-id="c169b-140">AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="c169b-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="c169b-141">新-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="c169b-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="c169b-142">移除-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="c169b-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)


