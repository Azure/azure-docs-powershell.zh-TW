---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: 6d7b82a3046b56b473140b6830a0b04333cba9b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128476"
---
# <span data-ttu-id="9dbdf-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9dbdf-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="9dbdf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9dbdf-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbdf-103">取得 Azure 資料工廠中邏輯閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="9dbdf-104">句法</span><span class="sxs-lookup"><span data-stu-id="9dbdf-104">SYNTAX</span></span>

### <span data-ttu-id="9dbdf-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="9dbdf-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9dbdf-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="9dbdf-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dbdf-107">說明</span><span class="sxs-lookup"><span data-stu-id="9dbdf-107">DESCRIPTION</span></span>
<span data-ttu-id="9dbdf-108">**AzDataFactoryGateway** Cmdlet 會取得 Azure 資料工廠中邏輯閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="9dbdf-109">如果您指定閘道的名稱，此 Cmdlet 會取得該閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="9dbdf-110">如果您沒有指定名稱，此 Cmdlet 會取得資料工廠所有閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="9dbdf-111">如果您想要將內部部署的 Microsoft SQL Server 作為連結的服務新增至資料工廠，您必須在內部部署電腦上安裝閘道。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="9dbdf-112">示例</span><span class="sxs-lookup"><span data-stu-id="9dbdf-112">EXAMPLES</span></span>

### <span data-ttu-id="9dbdf-113">範例1：取得資料工廠中的所有邏輯閘道</span><span class="sxs-lookup"><span data-stu-id="9dbdf-113">Example 1: Get all logical gateways in a data factory</span></span>
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

<span data-ttu-id="9dbdf-114">這個命令會在名為「ADF」的資源群組中，取得名為 WikiADF 之資料工廠之所有邏輯閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="9dbdf-115">範例2：在資料工廠中取得特定的邏輯閘道</span><span class="sxs-lookup"><span data-stu-id="9dbdf-115">Example 2: Get a specific logical gateway in a data factory</span></span>
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

<span data-ttu-id="9dbdf-116">這個命令會在名為 [ADF] 的資源群組中，取得名為 [WikiADF] 的 [資料工廠] 中名為 Gateway01 的邏輯閘道</span><span class="sxs-lookup"><span data-stu-id="9dbdf-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="9dbdf-117">參數</span><span class="sxs-lookup"><span data-stu-id="9dbdf-117">PARAMETERS</span></span>

### <span data-ttu-id="9dbdf-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="9dbdf-118">-DataFactory</span></span>
<span data-ttu-id="9dbdf-119">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="9dbdf-120">這個 Cmdlet 會取得此參數指定之資料工廠中邏輯閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9dbdf-121">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="9dbdf-121">-DataFactoryName</span></span>
<span data-ttu-id="9dbdf-122">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="9dbdf-123">這個 Cmdlet 會取得此參數指定之資料工廠中邏輯閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="9dbdf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dbdf-124">-DefaultProfile</span></span>
<span data-ttu-id="9dbdf-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9dbdf-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9dbdf-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="9dbdf-126">-Name</span></span>
<span data-ttu-id="9dbdf-127">指定要取得資訊之邏輯閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-127">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="9dbdf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dbdf-128">-ResourceGroupName</span></span>
<span data-ttu-id="9dbdf-129">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="9dbdf-130">這個 Cmdlet 會取得屬於此參數指定之群組之邏輯閘道的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9dbdf-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbdf-131">CommonParameters</span></span>
<span data-ttu-id="9dbdf-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbdf-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9dbdf-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbdf-134">輸入</span><span class="sxs-lookup"><span data-stu-id="9dbdf-134">INPUTS</span></span>

### <span data-ttu-id="9dbdf-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="9dbdf-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="9dbdf-136">System.object</span><span class="sxs-lookup"><span data-stu-id="9dbdf-136">System.String</span></span>

## <span data-ttu-id="9dbdf-137">輸出</span><span class="sxs-lookup"><span data-stu-id="9dbdf-137">OUTPUTS</span></span>

### <span data-ttu-id="9dbdf-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9dbdf-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="9dbdf-139">筆記</span><span class="sxs-lookup"><span data-stu-id="9dbdf-139">NOTES</span></span>
* <span data-ttu-id="9dbdf-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="9dbdf-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="9dbdf-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="9dbdf-141">RELATED LINKS</span></span>

[<span data-ttu-id="9dbdf-142">新-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9dbdf-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="9dbdf-143">移除-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9dbdf-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="9dbdf-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="9dbdf-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


