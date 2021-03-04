---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: ef13fd50877076fb11382623b5e7950098204997
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904073"
---
# <span data-ttu-id="aa17c-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="aa17c-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="aa17c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="aa17c-102">SYNOPSIS</span></span>
<span data-ttu-id="aa17c-103">獲得整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="aa17c-103">Gets an integration account map.</span></span>

## <span data-ttu-id="aa17c-104">語法</span><span class="sxs-lookup"><span data-stu-id="aa17c-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-MapType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa17c-105">描述</span><span class="sxs-lookup"><span data-stu-id="aa17c-105">DESCRIPTION</span></span>
<span data-ttu-id="aa17c-106">**Get-Az一AccountMap** Cmdlet 會從資源群組取得整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="aa17c-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="aa17c-107">指定整合帳戶名稱、資源組名和地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="aa17c-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="aa17c-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="aa17c-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="aa17c-109">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="aa17c-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="aa17c-110">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="aa17c-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="aa17c-111">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="aa17c-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="aa17c-112">例子</span><span class="sxs-lookup"><span data-stu-id="aa17c-112">EXAMPLES</span></span>

### <span data-ttu-id="aa17c-113">範例 1：取得整合帳戶地圖</span><span class="sxs-lookup"><span data-stu-id="aa17c-113">Example 1: Get an integration account map</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
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

<span data-ttu-id="aa17c-114">此命令會獲得指定資源群組中名為 IntegrationAccountMap47 的整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="aa17c-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="aa17c-115">範例 2：使用整合帳戶名稱取得整合帳戶地圖</span><span class="sxs-lookup"><span data-stu-id="aa17c-115">Example 2: Get integration account maps by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="aa17c-116">此命令會以整合帳戶名稱獲得整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="aa17c-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="aa17c-117">參數</span><span class="sxs-lookup"><span data-stu-id="aa17c-117">PARAMETERS</span></span>

### <span data-ttu-id="aa17c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa17c-118">-DefaultProfile</span></span>
<span data-ttu-id="aa17c-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="aa17c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa17c-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="aa17c-120">-MapName</span></span>
<span data-ttu-id="aa17c-121">指定整合帳戶地圖的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa17c-121">Specifies the name of an integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa17c-122">-MapType</span><span class="sxs-lookup"><span data-stu-id="aa17c-122">-MapType</span></span>
<span data-ttu-id="aa17c-123">整合帳戶地圖類型。</span><span class="sxs-lookup"><span data-stu-id="aa17c-123">The integration account map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa17c-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="aa17c-124">-Name</span></span>
<span data-ttu-id="aa17c-125">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa17c-125">Specifies the name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa17c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa17c-126">-ResourceGroupName</span></span>
<span data-ttu-id="aa17c-127">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa17c-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa17c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa17c-128">CommonParameters</span></span>
<span data-ttu-id="aa17c-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="aa17c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa17c-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="aa17c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa17c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="aa17c-131">INPUTS</span></span>

### <span data-ttu-id="aa17c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="aa17c-132">System.String</span></span>

## <span data-ttu-id="aa17c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="aa17c-133">OUTPUTS</span></span>

### <span data-ttu-id="aa17c-134">Microsoft.Azure.management.Logic.models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="aa17c-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="aa17c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="aa17c-135">NOTES</span></span>

## <span data-ttu-id="aa17c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa17c-136">RELATED LINKS</span></span>

[<span data-ttu-id="aa17c-137">New-AzCountAccountMap</span><span class="sxs-lookup"><span data-stu-id="aa17c-137">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="aa17c-138">Remove-Az有AccountMap</span><span class="sxs-lookup"><span data-stu-id="aa17c-138">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="aa17c-139">Set-AzCountAccountMap</span><span class="sxs-lookup"><span data-stu-id="aa17c-139">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


