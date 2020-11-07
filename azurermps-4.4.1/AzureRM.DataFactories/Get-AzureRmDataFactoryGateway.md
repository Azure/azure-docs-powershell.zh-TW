---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
ms.openlocfilehash: a90146480b0706d88f4ef7626b83008e08c22232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626330"
---
# <span data-ttu-id="5dd11-101">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="5dd11-101">Get-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="5dd11-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5dd11-102">SYNOPSIS</span></span>
<span data-ttu-id="5dd11-103">取得 Azure 資料工廠中邏輯閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5dd11-103">Gets information about logical gateways in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dd11-104">句法</span><span class="sxs-lookup"><span data-stu-id="5dd11-104">SYNTAX</span></span>

### <span data-ttu-id="5dd11-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="5dd11-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5dd11-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5dd11-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dd11-107">說明</span><span class="sxs-lookup"><span data-stu-id="5dd11-107">DESCRIPTION</span></span>
<span data-ttu-id="5dd11-108">**AzureRmDataFactoryGateway** Cmdlet 會取得 Azure 資料工廠中邏輯閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5dd11-108">The **Get-AzureRmDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="5dd11-109">如果您指定閘道的名稱，此 Cmdlet 會取得該閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5dd11-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="5dd11-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠所有閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5dd11-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>

<span data-ttu-id="5dd11-111">如果您想要將內部部署的 Microsoft SQL Server 作為連結的服務新增至資料工廠，您必須在內部部署電腦上安裝閘道。</span><span class="sxs-lookup"><span data-stu-id="5dd11-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="5dd11-112">示例</span><span class="sxs-lookup"><span data-stu-id="5dd11-112">EXAMPLES</span></span>

### <span data-ttu-id="5dd11-113">範例1：取得資料工廠中的所有邏輯閘道</span><span class="sxs-lookup"><span data-stu-id="5dd11-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
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

<span data-ttu-id="5dd11-114">這個命令會在名為「ADF」的資源群組中，取得名為 WikiADF 之資料工廠之所有邏輯閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5dd11-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="5dd11-115">範例2：在資料工廠中取得特定的邏輯閘道</span><span class="sxs-lookup"><span data-stu-id="5dd11-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
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

<span data-ttu-id="5dd11-116">這個命令會在名為 [ADF] 的資源群組中，取得名為 [WikiADF] 的 [資料工廠] 中名為 Gateway01 的邏輯閘道</span><span class="sxs-lookup"><span data-stu-id="5dd11-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="5dd11-117">參數</span><span class="sxs-lookup"><span data-stu-id="5dd11-117">PARAMETERS</span></span>

### <span data-ttu-id="5dd11-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5dd11-118">-DataFactory</span></span>
<span data-ttu-id="5dd11-119">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="5dd11-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="5dd11-120">這個 Cmdlet 會取得此參數指定之資料工廠中邏輯閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5dd11-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5dd11-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5dd11-121">-DataFactoryName</span></span>
<span data-ttu-id="5dd11-122">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="5dd11-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="5dd11-123">這個 Cmdlet 會取得此參數指定之資料工廠中邏輯閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5dd11-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="5dd11-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="5dd11-124">-Name</span></span>
<span data-ttu-id="5dd11-125">指定要取得資訊之邏輯閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="5dd11-125">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="5dd11-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dd11-126">-ResourceGroupName</span></span>
<span data-ttu-id="5dd11-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5dd11-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="5dd11-128">這個 Cmdlet 會取得屬於此參數指定之群組之邏輯閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5dd11-128">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5dd11-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dd11-129">-DefaultProfile</span></span>
<span data-ttu-id="5dd11-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5dd11-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dd11-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dd11-131">CommonParameters</span></span>
<span data-ttu-id="5dd11-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5dd11-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dd11-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5dd11-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dd11-134">輸入</span><span class="sxs-lookup"><span data-stu-id="5dd11-134">INPUTS</span></span>

## <span data-ttu-id="5dd11-135">輸出</span><span class="sxs-lookup"><span data-stu-id="5dd11-135">OUTPUTS</span></span>

### <span data-ttu-id="5dd11-136">[System.object]。清單 ' 1 [Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]]，Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="5dd11-136">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="5dd11-137">筆記</span><span class="sxs-lookup"><span data-stu-id="5dd11-137">NOTES</span></span>
* <span data-ttu-id="5dd11-138">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="5dd11-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="5dd11-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="5dd11-139">RELATED LINKS</span></span>

[<span data-ttu-id="5dd11-140">新-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="5dd11-140">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="5dd11-141">移除-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="5dd11-141">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="5dd11-142">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="5dd11-142">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


