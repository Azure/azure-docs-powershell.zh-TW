---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 8e86597292a9bcfef2163100d273d1e27daeb32a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965997"
---
# <span data-ttu-id="fbe09-101">Get-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="fbe09-101">Get-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="fbe09-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fbe09-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe09-103">取得 Azure 資料工廠的閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="fbe09-103">Gets gateway auth key for an Azure Data Factory.</span></span>

## <span data-ttu-id="fbe09-104">句法</span><span class="sxs-lookup"><span data-stu-id="fbe09-104">SYNTAX</span></span>

### <span data-ttu-id="fbe09-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="fbe09-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbe09-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fbe09-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbe09-107">說明</span><span class="sxs-lookup"><span data-stu-id="fbe09-107">DESCRIPTION</span></span>
<span data-ttu-id="fbe09-108">**AzDataFactoryGatewayAuthKey** Cmdlet 會取得指定 Azure 資料工廠閘道的閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="fbe09-108">The **Get-AzDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="fbe09-109">您可以使用這個 key1 或 key2 來向雲端服務註冊閘道。</span><span class="sxs-lookup"><span data-stu-id="fbe09-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="fbe09-110">示例</span><span class="sxs-lookup"><span data-stu-id="fbe09-110">EXAMPLES</span></span>

### <span data-ttu-id="fbe09-111">範例1：取得閘道的授權碼</span><span class="sxs-lookup"><span data-stu-id="fbe09-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="fbe09-112">這個命令會取得名為 MyGateway 的資料工廠閘道的閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="fbe09-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="fbe09-113">參數</span><span class="sxs-lookup"><span data-stu-id="fbe09-113">PARAMETERS</span></span>

### <span data-ttu-id="fbe09-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fbe09-114">-DataFactoryName</span></span>
<span data-ttu-id="fbe09-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="fbe09-115">The data factory name.</span></span>

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

### <span data-ttu-id="fbe09-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe09-116">-DefaultProfile</span></span>
<span data-ttu-id="fbe09-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fbe09-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbe09-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="fbe09-118">-GatewayName</span></span>
<span data-ttu-id="fbe09-119">資料工廠閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="fbe09-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="fbe09-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbe09-120">-InputObject</span></span>
<span data-ttu-id="fbe09-121">資料工廠物件</span><span class="sxs-lookup"><span data-stu-id="fbe09-121">The data factory object</span></span>

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

### <span data-ttu-id="fbe09-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe09-122">-ResourceGroupName</span></span>
<span data-ttu-id="fbe09-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbe09-123">The resource group name.</span></span>

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

### <span data-ttu-id="fbe09-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe09-124">CommonParameters</span></span>
<span data-ttu-id="fbe09-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fbe09-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe09-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fbe09-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe09-127">輸入</span><span class="sxs-lookup"><span data-stu-id="fbe09-127">INPUTS</span></span>

### <span data-ttu-id="fbe09-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fbe09-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="fbe09-129">System.object</span><span class="sxs-lookup"><span data-stu-id="fbe09-129">System.String</span></span>

## <span data-ttu-id="fbe09-130">輸出</span><span class="sxs-lookup"><span data-stu-id="fbe09-130">OUTPUTS</span></span>

### <span data-ttu-id="fbe09-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="fbe09-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="fbe09-132">筆記</span><span class="sxs-lookup"><span data-stu-id="fbe09-132">NOTES</span></span>
* <span data-ttu-id="fbe09-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="fbe09-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fbe09-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="fbe09-134">RELATED LINKS</span></span>

<span data-ttu-id="fbe09-135">[新-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
[新-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="fbe09-135">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[New-AzDataFactoryGatewayAuthKey](./New-AzDataFactoryGatewayAuthKey.md)</span></span>
