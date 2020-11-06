---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4F65A8B3-A250-41C1-9AA5-DBEB3193C401
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 6f1f58f5f25b3e3ef4782bcc0ea8a4b3170eed81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446774"
---
# <span data-ttu-id="be700-101">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="be700-101">Get-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="be700-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be700-102">SYNOPSIS</span></span>
<span data-ttu-id="be700-103">取得整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="be700-103">Gets an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be700-104">句法</span><span class="sxs-lookup"><span data-stu-id="be700-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountMap [-ResourceGroupName <String>] [-Name <String>] [-MapName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be700-105">說明</span><span class="sxs-lookup"><span data-stu-id="be700-105">DESCRIPTION</span></span>
<span data-ttu-id="be700-106">**AzureRmIntegrationAccountMap** Cmdlet 會從資源群組取得整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="be700-106">The **Get-AzureRmIntegrationAccountMap** cmdlet gets integration account map from a resource group.</span></span>
<span data-ttu-id="be700-107">指定整合帳戶名稱、資源群組名稱和地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="be700-107">Specifying the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="be700-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="be700-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="be700-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="be700-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="be700-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="be700-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="be700-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="be700-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="be700-112">示例</span><span class="sxs-lookup"><span data-stu-id="be700-112">EXAMPLES</span></span>

### <span data-ttu-id="be700-113">範例1：取得整合帳戶對應</span><span class="sxs-lookup"><span data-stu-id="be700-113">Example 1: Get an integration account map</span></span>
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

<span data-ttu-id="be700-114">這個命令會在指定的資源群組中取得名為 IntegrationAccountMap47 的整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="be700-114">This command gets an integration account map named IntegrationAccountMap47 in the specified resource group.</span></span>

### <span data-ttu-id="be700-115">範例2：依整合帳戶名稱取得整合帳戶對應</span><span class="sxs-lookup"><span data-stu-id="be700-115">Example 2: Get integration account maps by integration account name</span></span>
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

<span data-ttu-id="be700-116">這個命令會透過整合帳戶名稱來取得整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="be700-116">This command gets the integration account maps by integration account name.</span></span>

## <span data-ttu-id="be700-117">參數</span><span class="sxs-lookup"><span data-stu-id="be700-117">PARAMETERS</span></span>

### <span data-ttu-id="be700-118">-MapName</span><span class="sxs-lookup"><span data-stu-id="be700-118">-MapName</span></span>
<span data-ttu-id="be700-119">指定整合帳戶對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="be700-119">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="be700-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="be700-120">-Name</span></span>
<span data-ttu-id="be700-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="be700-121">Specifies the name for the integration account.</span></span>

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

### <span data-ttu-id="be700-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be700-122">-ResourceGroupName</span></span>
<span data-ttu-id="be700-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="be700-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="be700-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be700-124">-DefaultProfile</span></span>
<span data-ttu-id="be700-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be700-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be700-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be700-126">CommonParameters</span></span>
<span data-ttu-id="be700-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be700-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be700-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be700-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be700-129">輸入</span><span class="sxs-lookup"><span data-stu-id="be700-129">INPUTS</span></span>

## <span data-ttu-id="be700-130">輸出</span><span class="sxs-lookup"><span data-stu-id="be700-130">OUTPUTS</span></span>

### <span data-ttu-id="be700-131">IntegrationAccountMap 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="be700-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="be700-132">筆記</span><span class="sxs-lookup"><span data-stu-id="be700-132">NOTES</span></span>

## <span data-ttu-id="be700-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="be700-133">RELATED LINKS</span></span>

[<span data-ttu-id="be700-134">新-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="be700-134">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="be700-135">移除-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="be700-135">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="be700-136">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="be700-136">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


