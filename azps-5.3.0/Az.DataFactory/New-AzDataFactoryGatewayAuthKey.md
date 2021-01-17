---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 541cedecbad563be3e1a016dd651d3e93af44d1e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449407"
---
# <span data-ttu-id="b25d2-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="b25d2-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="b25d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b25d2-102">SYNOPSIS</span></span>
<span data-ttu-id="b25d2-103">建立 Azure 資料工廠閘道的授權金鑰。</span><span class="sxs-lookup"><span data-stu-id="b25d2-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="b25d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="b25d2-104">SYNTAX</span></span>

### <span data-ttu-id="b25d2-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="b25d2-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b25d2-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b25d2-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b25d2-107">說明</span><span class="sxs-lookup"><span data-stu-id="b25d2-107">DESCRIPTION</span></span>
<span data-ttu-id="b25d2-108">**新的-AzDataFactoryGatewayAuthKey** Cmdlet 會為指定的 Azure 資料工廠閘道建立閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="b25d2-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="b25d2-109">您可以使用此金鑰，透過雲端服務註冊閘道。</span><span class="sxs-lookup"><span data-stu-id="b25d2-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="b25d2-110">示例</span><span class="sxs-lookup"><span data-stu-id="b25d2-110">EXAMPLES</span></span>

### <span data-ttu-id="b25d2-111">範例1：為 Key1 建立閘道驗證金鑰</span><span class="sxs-lookup"><span data-stu-id="b25d2-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="b25d2-112">這個命令會為名為 MyGateway 的資料工廠閘道建立 Key 的閘道驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="b25d2-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="b25d2-113">參數</span><span class="sxs-lookup"><span data-stu-id="b25d2-113">PARAMETERS</span></span>

### <span data-ttu-id="b25d2-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b25d2-114">-DataFactoryName</span></span>
<span data-ttu-id="b25d2-115">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="b25d2-115">The data factory name.</span></span>

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

### <span data-ttu-id="b25d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b25d2-116">-DefaultProfile</span></span>
<span data-ttu-id="b25d2-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b25d2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b25d2-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="b25d2-118">-GatewayName</span></span>
<span data-ttu-id="b25d2-119">資料工廠閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="b25d2-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="b25d2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b25d2-120">-InputObject</span></span>
<span data-ttu-id="b25d2-121">資料工廠物件</span><span class="sxs-lookup"><span data-stu-id="b25d2-121">The data factory object</span></span>

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

### <span data-ttu-id="b25d2-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b25d2-122">-KeyName</span></span>
<span data-ttu-id="b25d2-123">要重新產生的閘道驗證金鑰的名稱，要麼是 "key" 或 "key2"。</span><span class="sxs-lookup"><span data-stu-id="b25d2-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

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

### <span data-ttu-id="b25d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b25d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="b25d2-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b25d2-125">The resource group name.</span></span>

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

### <span data-ttu-id="b25d2-126">-確認</span><span class="sxs-lookup"><span data-stu-id="b25d2-126">-Confirm</span></span>
<span data-ttu-id="b25d2-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b25d2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b25d2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b25d2-128">-WhatIf</span></span>
<span data-ttu-id="b25d2-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b25d2-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b25d2-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b25d2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b25d2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b25d2-131">CommonParameters</span></span>
<span data-ttu-id="b25d2-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b25d2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b25d2-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b25d2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b25d2-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b25d2-134">INPUTS</span></span>

### <span data-ttu-id="b25d2-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b25d2-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="b25d2-136">System.object</span><span class="sxs-lookup"><span data-stu-id="b25d2-136">System.String</span></span>

## <span data-ttu-id="b25d2-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b25d2-137">OUTPUTS</span></span>

### <span data-ttu-id="b25d2-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="b25d2-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="b25d2-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b25d2-139">NOTES</span></span>
* <span data-ttu-id="b25d2-140">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="b25d2-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b25d2-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b25d2-141">RELATED LINKS</span></span>

<span data-ttu-id="b25d2-142">[新-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
[AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="b25d2-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

