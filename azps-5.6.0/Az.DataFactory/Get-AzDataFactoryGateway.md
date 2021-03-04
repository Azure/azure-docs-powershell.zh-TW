---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: 80ff3a13014bcdc05191bcf5555abf2e029a831d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907782"
---
# <span data-ttu-id="5e9d5-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="5e9d5-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="5e9d5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5e9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9d5-103">在 Azure Data Factory 中，獲得邏輯閘道相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="5e9d5-104">語法</span><span class="sxs-lookup"><span data-stu-id="5e9d5-104">SYNTAX</span></span>

### <span data-ttu-id="5e9d5-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="5e9d5-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e9d5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5e9d5-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e9d5-107">描述</span><span class="sxs-lookup"><span data-stu-id="5e9d5-107">DESCRIPTION</span></span>
<span data-ttu-id="5e9d5-108">**Get-AzDataFactoryGateway** Cmdlet 會取得 Azure Data Factory 中邏輯閘道的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="5e9d5-109">如果您指定閘道的名稱，此 Cmdlet 會獲得該閘道的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="5e9d5-110">如果您未指定名稱，此 Cmdlet 會獲得資料工廠所有閘道的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="5e9d5-111">如果您想要將內部部署 Microsoft SQL Server 新增為數據工廠的連結服務，您必須在內部部署電腦上安裝閘道。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="5e9d5-112">例子</span><span class="sxs-lookup"><span data-stu-id="5e9d5-112">EXAMPLES</span></span>

### <span data-ttu-id="5e9d5-113">範例 1：在資料工廠中取得所有邏輯閘道</span><span class="sxs-lookup"><span data-stu-id="5e9d5-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
Name            : gateway1
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      : 
Name            : gateway2
Description     : 
Version         : 1.3.5338.1
Status          : Offline
VersionStatus   : UpToDate
CreateTime      : 8/29/2014 1:46:44 AM
RegisterTime    : 8/29/2014 1:48:36 AM
LastConnectTime : 8/29/2014 1:56:56 AM
ExpiryTime      :
```

<span data-ttu-id="5e9d5-114">此命令會針對名為 ADF 的資源群組中名為 WikiADF 的資料工廠，獲得所有邏輯閘道的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="5e9d5-115">範例 2：在資料工廠中取得特定的邏輯閘道</span><span class="sxs-lookup"><span data-stu-id="5e9d5-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
Name            : Gateway01
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      :
```

<span data-ttu-id="5e9d5-116">此命令會獲得名稱為 ADF 之資源群組中名稱為 WikiADF 之資料工廠中名為 Gateway01 的邏輯閘道相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="5e9d5-117">參數</span><span class="sxs-lookup"><span data-stu-id="5e9d5-117">PARAMETERS</span></span>

### <span data-ttu-id="5e9d5-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5e9d5-118">-DataFactory</span></span>
<span data-ttu-id="5e9d5-119">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="5e9d5-120">此 Cmdlet 會獲得此參數指定之資料工廠中邏輯閘道的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5e9d5-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5e9d5-121">-DataFactoryName</span></span>
<span data-ttu-id="5e9d5-122">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5e9d5-123">此 Cmdlet 會獲得此參數指定之資料工廠中邏輯閘道的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5e9d5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9d5-124">-DefaultProfile</span></span>
<span data-ttu-id="5e9d5-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="5e9d5-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e9d5-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e9d5-126">-Name</span></span>
<span data-ttu-id="5e9d5-127">指定要取得相關資訊的邏輯閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-127">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="5e9d5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e9d5-128">-ResourceGroupName</span></span>
<span data-ttu-id="5e9d5-129">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5e9d5-130">此 Cmdlet 會獲得屬於此參數指定之群組之邏輯閘道的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5e9d5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9d5-131">CommonParameters</span></span>
<span data-ttu-id="5e9d5-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9d5-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5e9d5-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9d5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="5e9d5-134">INPUTS</span></span>

### <span data-ttu-id="5e9d5-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5e9d5-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="5e9d5-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5e9d5-136">System.String</span></span>

## <span data-ttu-id="5e9d5-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5e9d5-137">OUTPUTS</span></span>

### <span data-ttu-id="5e9d5-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="5e9d5-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="5e9d5-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5e9d5-139">NOTES</span></span>
* <span data-ttu-id="5e9d5-140">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="5e9d5-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5e9d5-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e9d5-141">RELATED LINKS</span></span>

[<span data-ttu-id="5e9d5-142">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="5e9d5-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="5e9d5-143">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="5e9d5-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="5e9d5-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="5e9d5-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


