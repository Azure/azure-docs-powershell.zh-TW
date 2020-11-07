---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountMap.md
ms.openlocfilehash: 39e78dfc27c325b9327d8ca7c27d800d656e3536
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787161"
---
# <span data-ttu-id="cb05a-101">Get-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="cb05a-101">Get-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="cb05a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb05a-102">SYNOPSIS</span></span>
<span data-ttu-id="cb05a-103">取得整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="cb05a-103">Gets an integration account map.</span></span>

## <span data-ttu-id="cb05a-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb05a-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb05a-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb05a-105">DESCRIPTION</span></span>
<span data-ttu-id="cb05a-106">**AzIntegrationAccountMap** Cmdlet 會從資源群組取得整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="cb05a-106">The **Get-AzIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="cb05a-107">指定整合帳戶名稱、資源群組名稱和地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="cb05a-107">Specifying the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="cb05a-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="cb05a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cb05a-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="cb05a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cb05a-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="cb05a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cb05a-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="cb05a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cb05a-112">示例</span><span class="sxs-lookup"><span data-stu-id="cb05a-112">EXAMPLES</span></span>

### <span data-ttu-id="cb05a-113">範例1：取得整合帳戶對應</span><span class="sxs-lookup"><span data-stu-id="cb05a-113">Example 1: Get an integration account map</span></span>
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

<span data-ttu-id="cb05a-114">這個命令會在指定的資源群組中取得名為 IntegrationAccountMap47 的整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="cb05a-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="cb05a-115">範例2：依整合帳戶名稱取得整合帳戶對應</span><span class="sxs-lookup"><span data-stu-id="cb05a-115">Example 2: Get integration account maps by integration account name</span></span>
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

<span data-ttu-id="cb05a-116">這個命令會透過整合帳戶名稱來取得整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="cb05a-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="cb05a-117">參數</span><span class="sxs-lookup"><span data-stu-id="cb05a-117">PARAMETERS</span></span>

### <span data-ttu-id="cb05a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb05a-118">-DefaultProfile</span></span>
<span data-ttu-id="cb05a-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cb05a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb05a-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="cb05a-120">-MapName</span></span>
<span data-ttu-id="cb05a-121">指定整合帳戶對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb05a-121">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="cb05a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb05a-122">-Name</span></span>
<span data-ttu-id="cb05a-123">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb05a-123">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="cb05a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb05a-124">-ResourceGroupName</span></span>
<span data-ttu-id="cb05a-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb05a-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cb05a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb05a-126">CommonParameters</span></span>
<span data-ttu-id="cb05a-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb05a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb05a-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb05a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb05a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="cb05a-129">INPUTS</span></span>

### <span data-ttu-id="cb05a-130">System.object</span><span class="sxs-lookup"><span data-stu-id="cb05a-130">System.String</span></span>

## <span data-ttu-id="cb05a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="cb05a-131">OUTPUTS</span></span>

### <span data-ttu-id="cb05a-132">IntegrationAccountMap 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="cb05a-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="cb05a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="cb05a-133">NOTES</span></span>

## <span data-ttu-id="cb05a-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb05a-134">RELATED LINKS</span></span>

[<span data-ttu-id="cb05a-135">新-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="cb05a-135">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="cb05a-136">移除-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="cb05a-136">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="cb05a-137">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="cb05a-137">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


