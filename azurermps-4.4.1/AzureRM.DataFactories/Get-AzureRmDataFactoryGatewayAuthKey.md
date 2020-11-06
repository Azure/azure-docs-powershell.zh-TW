---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 9de30d10b34cf666b040c1b25b84e4afeae63a10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456776"
---
# <span data-ttu-id="99a94-101">Get-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="99a94-101">Get-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="99a94-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99a94-102">SYNOPSIS</span></span>
<span data-ttu-id="99a94-103">取得 Azure 資料工廠的閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="99a94-103">Gets gateway auth key for an Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99a94-104">句法</span><span class="sxs-lookup"><span data-stu-id="99a94-104">SYNTAX</span></span>

### <span data-ttu-id="99a94-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="99a94-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99a94-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="99a94-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGatewayAuthKey -InputObject <PSDataFactory> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99a94-107">說明</span><span class="sxs-lookup"><span data-stu-id="99a94-107">DESCRIPTION</span></span>
<span data-ttu-id="99a94-108">**AzureRmDataFactoryGatewayAuthKey** Cmdlet 會取得指定 Azure 資料工廠閘道的閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="99a94-108">The **Get-AzureRmDataFactoryGatewayAuthKey** cmdlet gets gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="99a94-109">您可以使用這個 key1 或 key2 來向雲端服務註冊閘道。</span><span class="sxs-lookup"><span data-stu-id="99a94-109">You register the gateway with a cloud service by using this key1 or key2 of this auth key.</span></span>

## <span data-ttu-id="99a94-110">示例</span><span class="sxs-lookup"><span data-stu-id="99a94-110">EXAMPLES</span></span>

### <span data-ttu-id="99a94-111">範例1：取得閘道的授權碼</span><span class="sxs-lookup"><span data-stu-id="99a94-111">Example 1: Gets auth key of a gateway</span></span>
```
PS C:\> Get-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@ZgBjjX6GfJcrzTQInEV9PoOqsDrqOmC
       gGHqUg1THLqA=
Key2 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@kFXxBdFCEBeL7LPB3hA3LqLd1uNFbyv
       YmWxtV4WD3JQ=
```

<span data-ttu-id="99a94-112">這個命令會取得名為 MyGateway 的資料工廠閘道的閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="99a94-112">This command gets gateway auth key for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="99a94-113">參數</span><span class="sxs-lookup"><span data-stu-id="99a94-113">PARAMETERS</span></span>

### <span data-ttu-id="99a94-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="99a94-114">-DataFactoryName</span></span>
<span data-ttu-id="99a94-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="99a94-115">The data factory name.</span></span>

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

### <span data-ttu-id="99a94-116">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="99a94-116">-GatewayName</span></span>
<span data-ttu-id="99a94-117">資料工廠閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="99a94-117">The data factory gateway name.</span></span>

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

### <span data-ttu-id="99a94-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99a94-118">-ResourceGroupName</span></span>
<span data-ttu-id="99a94-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="99a94-119">The resource group name.</span></span>

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

### <span data-ttu-id="99a94-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99a94-120">-DefaultProfile</span></span>
<span data-ttu-id="99a94-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="99a94-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99a94-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99a94-122">-InputObject</span></span>
<span data-ttu-id="99a94-123">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="99a94-123">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99a94-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99a94-124">CommonParameters</span></span>
<span data-ttu-id="99a94-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99a94-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99a94-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="99a94-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99a94-127">輸入</span><span class="sxs-lookup"><span data-stu-id="99a94-127">INPUTS</span></span>

### <span data-ttu-id="99a94-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="99a94-128">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="99a94-129">System.object</span><span class="sxs-lookup"><span data-stu-id="99a94-129">System.String</span></span>

## <span data-ttu-id="99a94-130">輸出</span><span class="sxs-lookup"><span data-stu-id="99a94-130">OUTPUTS</span></span>

### <span data-ttu-id="99a94-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="99a94-131">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="99a94-132">筆記</span><span class="sxs-lookup"><span data-stu-id="99a94-132">NOTES</span></span>
* <span data-ttu-id="99a94-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="99a94-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="99a94-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="99a94-134">RELATED LINKS</span></span>

<span data-ttu-id="99a94-135">[新-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
[新-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="99a94-135">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[New-AzureRmDataFactoryGatewayAuthKey](./New-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

