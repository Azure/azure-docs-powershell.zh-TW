---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: e58df40aa227e1c8132902c467c2dbcb881c7b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907662"
---
# <span data-ttu-id="3e748-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="3e748-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="3e748-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3e748-102">SYNOPSIS</span></span>
<span data-ttu-id="3e748-103">建立 Azure Data Factory 閘道的驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="3e748-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="3e748-104">語法</span><span class="sxs-lookup"><span data-stu-id="3e748-104">SYNTAX</span></span>

### <span data-ttu-id="3e748-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="3e748-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e748-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3e748-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e748-107">描述</span><span class="sxs-lookup"><span data-stu-id="3e748-107">DESCRIPTION</span></span>
<span data-ttu-id="3e748-108">**New-AzDataFactoryGatewayAuthKey** Cmdlet 會為指定的 Azure Data Factory 閘道建立閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="3e748-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="3e748-109">您可以使用此金鑰向雲端服務註冊閘道。</span><span class="sxs-lookup"><span data-stu-id="3e748-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="3e748-110">例子</span><span class="sxs-lookup"><span data-stu-id="3e748-110">EXAMPLES</span></span>

### <span data-ttu-id="3e748-111">範例 1：為 Key1 建立閘道驗證金鑰</span><span class="sxs-lookup"><span data-stu-id="3e748-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="3e748-112">此命令會針對名為 MyGateway 的資料工廠閘道建立 Key1 的閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="3e748-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="3e748-113">參數</span><span class="sxs-lookup"><span data-stu-id="3e748-113">PARAMETERS</span></span>

### <span data-ttu-id="3e748-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3e748-114">-DataFactoryName</span></span>
<span data-ttu-id="3e748-115">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="3e748-115">The data factory name.</span></span>

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

### <span data-ttu-id="3e748-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e748-116">-DefaultProfile</span></span>
<span data-ttu-id="3e748-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="3e748-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e748-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="3e748-118">-GatewayName</span></span>
<span data-ttu-id="3e748-119">資料工廠閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="3e748-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="3e748-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e748-120">-InputObject</span></span>
<span data-ttu-id="3e748-121">資料工廠物件</span><span class="sxs-lookup"><span data-stu-id="3e748-121">The data factory object</span></span>

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

### <span data-ttu-id="3e748-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3e748-122">-KeyName</span></span>
<span data-ttu-id="3e748-123">要重新產生閘道驗證金鑰的名稱，可以是 'key1' 或 'key2'。</span><span class="sxs-lookup"><span data-stu-id="3e748-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e748-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e748-124">-ResourceGroupName</span></span>
<span data-ttu-id="3e748-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3e748-125">The resource group name.</span></span>

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

### <span data-ttu-id="3e748-126">-確認</span><span class="sxs-lookup"><span data-stu-id="3e748-126">-Confirm</span></span>
<span data-ttu-id="3e748-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3e748-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e748-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e748-128">-WhatIf</span></span>
<span data-ttu-id="3e748-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3e748-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e748-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e748-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e748-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e748-131">CommonParameters</span></span>
<span data-ttu-id="3e748-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3e748-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e748-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3e748-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e748-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3e748-134">INPUTS</span></span>

### <span data-ttu-id="3e748-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3e748-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="3e748-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3e748-136">System.String</span></span>

## <span data-ttu-id="3e748-137">輸出</span><span class="sxs-lookup"><span data-stu-id="3e748-137">OUTPUTS</span></span>

### <span data-ttu-id="3e748-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="3e748-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="3e748-139">筆記</span><span class="sxs-lookup"><span data-stu-id="3e748-139">NOTES</span></span>
* <span data-ttu-id="3e748-140">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="3e748-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="3e748-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e748-141">RELATED LINKS</span></span>

<span data-ttu-id="3e748-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="3e748-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

