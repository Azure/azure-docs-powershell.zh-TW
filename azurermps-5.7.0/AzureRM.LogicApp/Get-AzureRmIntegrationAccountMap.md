---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 340320ee102317069e81806ba9a7831dc1077368
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452211"
---
# <span data-ttu-id="b9335-101">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b9335-101">Get-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="b9335-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9335-102">SYNOPSIS</span></span>
<span data-ttu-id="b9335-103">取得整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="b9335-103">Gets an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9335-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9335-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9335-105">說明</span><span class="sxs-lookup"><span data-stu-id="b9335-105">DESCRIPTION</span></span>
<span data-ttu-id="b9335-106">**AzureRmIntegrationAccountMap** Cmdlet 會從資源群組取得整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="b9335-106">The **Get-AzureRmIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="b9335-107">指定整合帳戶名稱、資源群組名稱和地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="b9335-107">Specifying the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="b9335-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="b9335-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b9335-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="b9335-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b9335-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="b9335-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b9335-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="b9335-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b9335-112">示例</span><span class="sxs-lookup"><span data-stu-id="b9335-112">EXAMPLES</span></span>

### <span data-ttu-id="b9335-113">範例1：取得整合帳戶對應</span><span class="sxs-lookup"><span data-stu-id="b9335-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="b9335-114">這個命令會在指定的資源群組中取得名為 IntegrationAccountMap47 的整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="b9335-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="b9335-115">範例2：依整合帳戶名稱取得整合帳戶對應</span><span class="sxs-lookup"><span data-stu-id="b9335-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
Name                 : IntegrationAccountMap47
Type                 : Microsoft.Logic/integrationAccounts/maps
CreatedTime          : 3/24/2016 10:34:26 PM
ChangedTime          : 3/24/2016 10:34:26 PM
MapType              : Xslt
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts8811f0155a364b5e9618ba28f7180601/99D1E_XSLT_INTEGRATIONACCOUNT
                       MAP1-9A960F9B71C844CDB09D4922B3BCFF61?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 3056
Metadata             :
```

<span data-ttu-id="b9335-116">這個命令會透過整合帳戶名稱來取得整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="b9335-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="b9335-117">參數</span><span class="sxs-lookup"><span data-stu-id="b9335-117">PARAMETERS</span></span>

### <span data-ttu-id="b9335-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9335-118">-DefaultProfile</span></span>
<span data-ttu-id="b9335-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b9335-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9335-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="b9335-120">-MapName</span></span>
<span data-ttu-id="b9335-121">指定整合帳戶對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9335-121">Specifies the name of an integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9335-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b9335-122">-Name</span></span>
<span data-ttu-id="b9335-123">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9335-123">Specifies the name for the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9335-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9335-124">-ResourceGroupName</span></span>
<span data-ttu-id="b9335-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9335-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9335-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9335-126">CommonParameters</span></span>
<span data-ttu-id="b9335-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9335-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9335-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b9335-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9335-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b9335-129">INPUTS</span></span>

### <span data-ttu-id="b9335-130">所有</span><span class="sxs-lookup"><span data-stu-id="b9335-130">None</span></span>
<span data-ttu-id="b9335-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b9335-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b9335-132">輸出</span><span class="sxs-lookup"><span data-stu-id="b9335-132">OUTPUTS</span></span>

### <span data-ttu-id="b9335-133">IntegrationAccountMap 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="b9335-133">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="b9335-134">筆記</span><span class="sxs-lookup"><span data-stu-id="b9335-134">NOTES</span></span>

## <span data-ttu-id="b9335-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9335-135">RELATED LINKS</span></span>

[<span data-ttu-id="b9335-136">新-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b9335-136">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="b9335-137">移除-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b9335-137">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="b9335-138">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b9335-138">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


