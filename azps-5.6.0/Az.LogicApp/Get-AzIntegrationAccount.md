---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: c519a747a36db3ed2a2365052ac00a1166c45aed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907122"
---
# <span data-ttu-id="1c6ff-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1c6ff-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="1c6ff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1c6ff-102">SYNOPSIS</span></span>
<span data-ttu-id="1c6ff-103">獲得整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="1c6ff-103">Gets integration accounts.</span></span>

## <span data-ttu-id="1c6ff-104">語法</span><span class="sxs-lookup"><span data-stu-id="1c6ff-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c6ff-105">描述</span><span class="sxs-lookup"><span data-stu-id="1c6ff-105">DESCRIPTION</span></span>
<span data-ttu-id="1c6ff-106">**Get-Az一Account** Cmdlet 會從資源群組取得整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="1c6ff-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="1c6ff-107">指定整合帳戶名稱和資源組名。</span><span class="sxs-lookup"><span data-stu-id="1c6ff-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="1c6ff-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="1c6ff-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1c6ff-109">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="1c6ff-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1c6ff-110">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="1c6ff-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1c6ff-111">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="1c6ff-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1c6ff-112">例子</span><span class="sxs-lookup"><span data-stu-id="1c6ff-112">EXAMPLES</span></span>

### <span data-ttu-id="1c6ff-113">範例 1：按名稱取得整合帳戶</span><span class="sxs-lookup"><span data-stu-id="1c6ff-113">Example 1: Get an integration account by name</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="1c6ff-114">此命令會從指定的資源群組中，獲得一個名為 IntegrationAccount31 的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="1c6ff-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="1c6ff-115">範例 2：在資源群組中取得整合帳戶</span><span class="sxs-lookup"><span data-stu-id="1c6ff-115">Example 2: Get integration accounts in a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccount -ResourceGroupName "ResourceGroup11"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup1/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="1c6ff-116">此命令會從名為 ResourceGroup11 的資源群組中，獲得整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="1c6ff-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="1c6ff-117">範例 3：取得所有整合帳戶</span><span class="sxs-lookup"><span data-stu-id="1c6ff-117">Example 3: Get all integration accounts</span></span>
```
PS C:\>Get-AzIntegrationAccount
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="1c6ff-118">此命令會獲得 Azure 訂閱中所有的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="1c6ff-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="1c6ff-119">參數</span><span class="sxs-lookup"><span data-stu-id="1c6ff-119">PARAMETERS</span></span>

### <span data-ttu-id="1c6ff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c6ff-120">-DefaultProfile</span></span>
<span data-ttu-id="1c6ff-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1c6ff-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c6ff-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c6ff-122">-Name</span></span>
<span data-ttu-id="1c6ff-123">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c6ff-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="1c6ff-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c6ff-124">-ResourceGroupName</span></span>
<span data-ttu-id="1c6ff-125">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c6ff-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1c6ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c6ff-126">CommonParameters</span></span>
<span data-ttu-id="1c6ff-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1c6ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c6ff-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1c6ff-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c6ff-129">輸入</span><span class="sxs-lookup"><span data-stu-id="1c6ff-129">INPUTS</span></span>

### <span data-ttu-id="1c6ff-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1c6ff-130">System.String</span></span>

## <span data-ttu-id="1c6ff-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1c6ff-131">OUTPUTS</span></span>

### <span data-ttu-id="1c6ff-132">Microsoft.Azure.management.Logic.models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="1c6ff-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="1c6ff-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1c6ff-133">NOTES</span></span>

## <span data-ttu-id="1c6ff-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c6ff-134">RELATED LINKS</span></span>

[<span data-ttu-id="1c6ff-135">Get-AzCountAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="1c6ff-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="1c6ff-136">New-AzCountAccount</span><span class="sxs-lookup"><span data-stu-id="1c6ff-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="1c6ff-137">Remove-AzCountAccount</span><span class="sxs-lookup"><span data-stu-id="1c6ff-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="1c6ff-138">Set-AzCountAccount</span><span class="sxs-lookup"><span data-stu-id="1c6ff-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


