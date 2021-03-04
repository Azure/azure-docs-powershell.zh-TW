---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 7987f014b08250975a2a25323122a081d508b036
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907781"
---
# <span data-ttu-id="a62dc-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="a62dc-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="a62dc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a62dc-102">SYNOPSIS</span></span>
<span data-ttu-id="a62dc-103">為 Azure Data Factory 獲得閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="a62dc-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="a62dc-104">語法</span><span class="sxs-lookup"><span data-stu-id="a62dc-104">SYNTAX</span></span>

### <span data-ttu-id="a62dc-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="a62dc-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a62dc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a62dc-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a62dc-107">描述</span><span class="sxs-lookup"><span data-stu-id="a62dc-107">DESCRIPTION</span></span>
<span data-ttu-id="a62dc-108">**Get-AzDataFactoryGatewayAuthKey** Cmdlet 會取得指定 Azure Data Factory 閘道的閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="a62dc-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="a62dc-109">您可以使用此驗證金鑰的金鑰1 或 key2，向雲端服務註冊閘道。</span><span class="sxs-lookup"><span data-stu-id="a62dc-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="a62dc-110">例子</span><span class="sxs-lookup"><span data-stu-id="a62dc-110">EXAMPLES</span></span>

### <span data-ttu-id="a62dc-111">範例 1：獲取閘道的驗證金鑰</span><span class="sxs-lookup"><span data-stu-id="a62dc-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="a62dc-112">此命令會針對名為 MyGateway 的資料工廠閘道，獲得閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="a62dc-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="a62dc-113">參數</span><span class="sxs-lookup"><span data-stu-id="a62dc-113">PARAMETERS</span></span>

### <span data-ttu-id="a62dc-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a62dc-114">-DataFactoryName</span></span>
<span data-ttu-id="a62dc-115">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="a62dc-115">The data factory name.</span></span>

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

### <span data-ttu-id="a62dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a62dc-116">-DefaultProfile</span></span>
<span data-ttu-id="a62dc-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a62dc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a62dc-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="a62dc-118">-GatewayName</span></span>
<span data-ttu-id="a62dc-119">資料工廠閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="a62dc-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="a62dc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a62dc-120">-InputObject</span></span>
<span data-ttu-id="a62dc-121">資料工廠物件</span><span class="sxs-lookup"><span data-stu-id="a62dc-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a62dc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a62dc-122">-ResourceGroupName</span></span>
<span data-ttu-id="a62dc-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a62dc-123">The resource group name.</span></span>

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

### <span data-ttu-id="a62dc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a62dc-124">CommonParameters</span></span>
<span data-ttu-id="a62dc-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a62dc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a62dc-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a62dc-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a62dc-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a62dc-127">INPUTS</span></span>

### <span data-ttu-id="a62dc-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a62dc-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="a62dc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a62dc-129">System.String</span></span>

## <span data-ttu-id="a62dc-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a62dc-130">OUTPUTS</span></span>

### <span data-ttu-id="a62dc-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="a62dc-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="a62dc-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a62dc-132">NOTES</span></span>
* <span data-ttu-id="a62dc-133">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="a62dc-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a62dc-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="a62dc-134">RELATED LINKS</span></span>

<span data-ttu-id="a62dc-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="a62dc-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>

