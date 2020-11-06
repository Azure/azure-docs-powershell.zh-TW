---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: cf7632cc88f55e010a3da3d9ba543c391bbcc214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444615"
---
# <span data-ttu-id="fbc12-101">New-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="fbc12-101">New-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="fbc12-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fbc12-102">SYNOPSIS</span></span>
<span data-ttu-id="fbc12-103">建立 Azure 資料工廠閘道的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="fbc12-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbc12-104">句法</span><span class="sxs-lookup"><span data-stu-id="fbc12-104">SYNTAX</span></span>

### <span data-ttu-id="fbc12-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="fbc12-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbc12-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fbc12-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbc12-107">說明</span><span class="sxs-lookup"><span data-stu-id="fbc12-107">DESCRIPTION</span></span>
<span data-ttu-id="fbc12-108">**新的-AzureRmDataFactoryGatewayAuthKey** Cmdlet 會為指定的 Azure 資料工廠閘道建立閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="fbc12-108">The **New-AzureRmDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="fbc12-109">您可以使用此金鑰，透過雲端服務註冊閘道。</span><span class="sxs-lookup"><span data-stu-id="fbc12-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="fbc12-110">示例</span><span class="sxs-lookup"><span data-stu-id="fbc12-110">EXAMPLES</span></span>

### <span data-ttu-id="fbc12-111">範例1：為 Key1 建立閘道驗證金鑰</span><span class="sxs-lookup"><span data-stu-id="fbc12-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="fbc12-112">這個命令會為名為 MyGateway 的資料工廠閘道建立 Key 的閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="fbc12-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="fbc12-113">參數</span><span class="sxs-lookup"><span data-stu-id="fbc12-113">PARAMETERS</span></span>

### <span data-ttu-id="fbc12-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fbc12-114">-DataFactoryName</span></span>
<span data-ttu-id="fbc12-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="fbc12-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc12-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbc12-116">-DefaultProfile</span></span>
<span data-ttu-id="fbc12-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fbc12-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbc12-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="fbc12-118">-GatewayName</span></span>
<span data-ttu-id="fbc12-119">資料工廠閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="fbc12-119">The data factory gateway name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc12-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbc12-120">-InputObject</span></span>
<span data-ttu-id="fbc12-121">資料工廠物件</span><span class="sxs-lookup"><span data-stu-id="fbc12-121">The data factory object</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc12-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fbc12-122">-KeyName</span></span>
<span data-ttu-id="fbc12-123">要重新產生的閘道驗證金鑰的名稱，要麼是 "key" 或 "key2"。</span><span class="sxs-lookup"><span data-stu-id="fbc12-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: key1, key2

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc12-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbc12-124">-ResourceGroupName</span></span>
<span data-ttu-id="fbc12-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbc12-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbc12-126">-確認</span><span class="sxs-lookup"><span data-stu-id="fbc12-126">-Confirm</span></span>
<span data-ttu-id="fbc12-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fbc12-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbc12-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbc12-128">-WhatIf</span></span>
<span data-ttu-id="fbc12-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fbc12-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fbc12-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fbc12-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbc12-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbc12-131">CommonParameters</span></span>
<span data-ttu-id="fbc12-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fbc12-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbc12-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fbc12-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbc12-134">輸入</span><span class="sxs-lookup"><span data-stu-id="fbc12-134">INPUTS</span></span>

### <span data-ttu-id="fbc12-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fbc12-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="fbc12-136">System.object</span><span class="sxs-lookup"><span data-stu-id="fbc12-136">System.String</span></span>

## <span data-ttu-id="fbc12-137">輸出</span><span class="sxs-lookup"><span data-stu-id="fbc12-137">OUTPUTS</span></span>

### <span data-ttu-id="fbc12-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="fbc12-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="fbc12-139">筆記</span><span class="sxs-lookup"><span data-stu-id="fbc12-139">NOTES</span></span>
* <span data-ttu-id="fbc12-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="fbc12-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fbc12-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="fbc12-141">RELATED LINKS</span></span>

<span data-ttu-id="fbc12-142">[新-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
[AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="fbc12-142">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

