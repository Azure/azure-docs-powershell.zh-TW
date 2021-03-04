---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: c0cdd988c71a1943063fd7d07cd5e1b6d1c76f83
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914061"
---
# <span data-ttu-id="4efa9-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4efa9-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="4efa9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4efa9-102">SYNOPSIS</span></span>
<span data-ttu-id="4efa9-103">在 Azure Data Factory 中設定閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="4efa9-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="4efa9-104">語法</span><span class="sxs-lookup"><span data-stu-id="4efa9-104">SYNTAX</span></span>

### <span data-ttu-id="4efa9-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="4efa9-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4efa9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4efa9-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4efa9-107">描述</span><span class="sxs-lookup"><span data-stu-id="4efa9-107">DESCRIPTION</span></span>
<span data-ttu-id="4efa9-108">**Set-AzDataFactoryGateway** Cmdlet 會設定 Azure Data Factory 中指定閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="4efa9-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="4efa9-109">例子</span><span class="sxs-lookup"><span data-stu-id="4efa9-109">EXAMPLES</span></span>

### <span data-ttu-id="4efa9-110">範例 1：設定閘道的描述</span><span class="sxs-lookup"><span data-stu-id="4efa9-110">Example 1: Set the description for a gateway</span></span>
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

<span data-ttu-id="4efa9-111">此命令會針對名為 WikiADF 的資料工廠中名為 ContosoGateway 的閘道設定描述。</span><span class="sxs-lookup"><span data-stu-id="4efa9-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="4efa9-112">描述參數會指定新的描述。</span><span class="sxs-lookup"><span data-stu-id="4efa9-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="4efa9-113">參數</span><span class="sxs-lookup"><span data-stu-id="4efa9-113">PARAMETERS</span></span>

### <span data-ttu-id="4efa9-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4efa9-114">-DataFactory</span></span>
<span data-ttu-id="4efa9-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="4efa9-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4efa9-116">此 Cmdlet 會在此參數指定的資料工廠中設定閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="4efa9-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4efa9-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4efa9-117">-DataFactoryName</span></span>
<span data-ttu-id="4efa9-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="4efa9-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4efa9-119">此 Cmdlet 會在此參數指定的資料工廠中設定閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="4efa9-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4efa9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4efa9-120">-DefaultProfile</span></span>
<span data-ttu-id="4efa9-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="4efa9-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4efa9-122">-描述</span><span class="sxs-lookup"><span data-stu-id="4efa9-122">-Description</span></span>
<span data-ttu-id="4efa9-123">指定閘道的描述。</span><span class="sxs-lookup"><span data-stu-id="4efa9-123">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="4efa9-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="4efa9-124">-Name</span></span>
<span data-ttu-id="4efa9-125">指定要設定描述的閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="4efa9-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="4efa9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4efa9-126">-ResourceGroupName</span></span>
<span data-ttu-id="4efa9-127">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4efa9-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4efa9-128">此 Cmdlet 會針對屬於此參數指定群組的閘道設定描述。</span><span class="sxs-lookup"><span data-stu-id="4efa9-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4efa9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4efa9-129">CommonParameters</span></span>
<span data-ttu-id="4efa9-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4efa9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4efa9-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4efa9-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4efa9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="4efa9-132">INPUTS</span></span>

### <span data-ttu-id="4efa9-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="4efa9-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="4efa9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4efa9-134">System.String</span></span>

## <span data-ttu-id="4efa9-135">輸出</span><span class="sxs-lookup"><span data-stu-id="4efa9-135">OUTPUTS</span></span>

### <span data-ttu-id="4efa9-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4efa9-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="4efa9-137">筆記</span><span class="sxs-lookup"><span data-stu-id="4efa9-137">NOTES</span></span>
* <span data-ttu-id="4efa9-138">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="4efa9-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4efa9-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="4efa9-139">RELATED LINKS</span></span>

[<span data-ttu-id="4efa9-140">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4efa9-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="4efa9-141">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4efa9-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="4efa9-142">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4efa9-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)


