---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 8546C3FE-5396-4027-BF33-F98F6C018A67
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayKey.md
ms.openlocfilehash: f1676d385b23711e71fbec5fb5d9131add4daaf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449629"
---
# <span data-ttu-id="b6128-101">New-AzureRmDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="b6128-101">New-AzureRmDataFactoryGatewayKey</span></span>

## <span data-ttu-id="b6128-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6128-102">SYNOPSIS</span></span>
<span data-ttu-id="b6128-103">建立 Azure 資料工廠的閘道金鑰。</span><span class="sxs-lookup"><span data-stu-id="b6128-103">Creates a gateway key for an Azure Data Factory.</span></span> <span data-ttu-id="b6128-104">此 Cmdlet 已棄用，您應該改為使用 **新的 AzureRmDataFactoryGatewayAuthKey** 。</span><span class="sxs-lookup"><span data-stu-id="b6128-104">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6128-105">句法</span><span class="sxs-lookup"><span data-stu-id="b6128-105">SYNTAX</span></span>

### <span data-ttu-id="b6128-106">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="b6128-106">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6128-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b6128-107">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayKey [-DataFactory] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6128-108">說明</span><span class="sxs-lookup"><span data-stu-id="b6128-108">DESCRIPTION</span></span>
<span data-ttu-id="b6128-109">**新的-AzureRmDataFactoryGatewayKey** Cmdlet 會為指定的 Azure 資料工廠閘道建立閘道金鑰。</span><span class="sxs-lookup"><span data-stu-id="b6128-109">The **New-AzureRmDataFactoryGatewayKey** cmdlet creates a gateway key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="b6128-110">您可以使用此金鑰，透過雲端服務註冊閘道。</span><span class="sxs-lookup"><span data-stu-id="b6128-110">You register the gateway with a cloud service by using this key.</span></span> <span data-ttu-id="b6128-111">此 Cmdlet 已棄用，您應該改為使用 **新的 AzureRmDataFactoryGatewayAuthKey** 。</span><span class="sxs-lookup"><span data-stu-id="b6128-111">This cmdlet is deprecated, and you should use **New-AzureRmDataFactoryGatewayAuthKey** instead.</span></span>

## <span data-ttu-id="b6128-112">示例</span><span class="sxs-lookup"><span data-stu-id="b6128-112">EXAMPLES</span></span>

### <span data-ttu-id="b6128-113">範例1：建立閘道金鑰</span><span class="sxs-lookup"><span data-stu-id="b6128-113">Example 1: Create a gateway key</span></span>
```
PS C:\>New-AzureRmDataFactoryGatewayKey -ResourceGroupName "ADF" -GatewayName "ContosoGateway" -DataFactoryName "WikiADF" | Format-List
GatewayKey : ADF#40cbb3d9-2736-4794-a8a6-e6b839b4894f@a2d875ce-c9d7-4b8b-ad65-dd3ebbb9a940@8c0d1801-e863-44af-82e6-fb2f0c00f2ae@xz#Y9R0NhAeH3u7wgnrJyiWj4Y/QIhH4fFilIdzZgwsVQA=
```

<span data-ttu-id="b6128-114">這個命令會為名為 ContosoGateway 的資料工廠閘道建立閘道金鑰，然後使用管線運算子將閘道金鑰傳送至 Format-List Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6128-114">This command creates a gateway key for the data factory gateway named ContosoGateway, and then passes the gateway key to the Format-List cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b6128-115">如需詳細資訊，請輸入 `Get-Help Format-List` 。</span><span class="sxs-lookup"><span data-stu-id="b6128-115">For more information, type `Get-Help Format-List`.</span></span>

## <span data-ttu-id="b6128-116">參數</span><span class="sxs-lookup"><span data-stu-id="b6128-116">PARAMETERS</span></span>

### <span data-ttu-id="b6128-117">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b6128-117">-DataFactory</span></span>
<span data-ttu-id="b6128-118">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="b6128-118">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b6128-119">這個 Cmdlet 會為此參數指定的資料工廠建立閘道金鑰。</span><span class="sxs-lookup"><span data-stu-id="b6128-119">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6128-120">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b6128-120">-DataFactoryName</span></span>
<span data-ttu-id="b6128-121">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6128-121">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b6128-122">這個 Cmdlet 會為此參數指定的資料工廠建立閘道金鑰。</span><span class="sxs-lookup"><span data-stu-id="b6128-122">This cmdlet creates a gateway key for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6128-123">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="b6128-123">-GatewayName</span></span>
<span data-ttu-id="b6128-124">指定閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6128-124">Specifies the name of the gateway.</span></span>
<span data-ttu-id="b6128-125">這個 Cmdlet 會為此參數指定的閘道建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="b6128-125">This cmdlet creates a key for the gateway that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6128-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6128-126">-ResourceGroupName</span></span>
<span data-ttu-id="b6128-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6128-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b6128-128">這個 Cmdlet 會為屬於此參數指定之群組的閘道建立金鑰。</span><span class="sxs-lookup"><span data-stu-id="b6128-128">This cmdlet creates a key for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b6128-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6128-129">-DefaultProfile</span></span>
<span data-ttu-id="b6128-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6128-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6128-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6128-131">CommonParameters</span></span>
<span data-ttu-id="b6128-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6128-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6128-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b6128-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6128-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b6128-134">INPUTS</span></span>

## <span data-ttu-id="b6128-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b6128-135">OUTPUTS</span></span>

### <span data-ttu-id="b6128-136">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span><span class="sxs-lookup"><span data-stu-id="b6128-136">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGatewayKey</span></span>

## <span data-ttu-id="b6128-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b6128-137">NOTES</span></span>
* <span data-ttu-id="b6128-138">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="b6128-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b6128-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6128-139">RELATED LINKS</span></span>

<span data-ttu-id="b6128-140">[新-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
[AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md) 
[新-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="b6128-140">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>


