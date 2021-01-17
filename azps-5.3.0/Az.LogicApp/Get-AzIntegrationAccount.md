---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BCF2086-05FA-43FB-9D19-7277374CB03E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccount.md
ms.openlocfilehash: b13e7b63994f71f51f321428472169aea52e92f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449074"
---
# <span data-ttu-id="62729-101">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="62729-101">Get-AzIntegrationAccount</span></span>

## <span data-ttu-id="62729-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62729-102">SYNOPSIS</span></span>
<span data-ttu-id="62729-103">取得整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="62729-103">Gets integration accounts.</span></span>

## <span data-ttu-id="62729-104">句法</span><span class="sxs-lookup"><span data-stu-id="62729-104">SYNTAX</span></span>

```
Get-AzIntegrationAccount [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62729-105">說明</span><span class="sxs-lookup"><span data-stu-id="62729-105">DESCRIPTION</span></span>
<span data-ttu-id="62729-106">**AzIntegrationAccount** Cmdlet 會從資源群組取得整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="62729-106">The **Get-AzIntegrationAccount** cmdlet gets integration accounts from a resource group.</span></span> <span data-ttu-id="62729-107">指定整合帳戶名稱和資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="62729-107">Specify an integration account name and resource group name.</span></span>
<span data-ttu-id="62729-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="62729-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="62729-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="62729-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="62729-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="62729-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="62729-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="62729-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="62729-112">示例</span><span class="sxs-lookup"><span data-stu-id="62729-112">EXAMPLES</span></span>

### <span data-ttu-id="62729-113">範例1：依名稱取得整合帳戶</span><span class="sxs-lookup"><span data-stu-id="62729-113">Example 1: Get an integration account by name</span></span>
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

<span data-ttu-id="62729-114">這個命令會從指定的資源群組中取得名為 IntegrationAccount31 的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="62729-114">This command gets an integration account named IntegrationAccount31 from the specified resource group.</span></span>

### <span data-ttu-id="62729-115">範例2：取得資源群組中的整合帳戶</span><span class="sxs-lookup"><span data-stu-id="62729-115">Example 2: Get integration accounts in a resource group</span></span>
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

<span data-ttu-id="62729-116">這個命令會從名為 ResourceGroup11 的資源群組中取得整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="62729-116">This command gets integration accounts from a resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="62729-117">範例3：取得所有整合帳戶</span><span class="sxs-lookup"><span data-stu-id="62729-117">Example 3: Get all integration accounts</span></span>
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

<span data-ttu-id="62729-118">這個命令會取得 Azure 訂閱中的所有整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="62729-118">This command gets all the integration accounts in your Azure subscription.</span></span>

## <span data-ttu-id="62729-119">參數</span><span class="sxs-lookup"><span data-stu-id="62729-119">PARAMETERS</span></span>

### <span data-ttu-id="62729-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62729-120">-DefaultProfile</span></span>
<span data-ttu-id="62729-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="62729-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62729-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="62729-122">-Name</span></span>
<span data-ttu-id="62729-123">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="62729-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="62729-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62729-124">-ResourceGroupName</span></span>
<span data-ttu-id="62729-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="62729-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="62729-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62729-126">CommonParameters</span></span>
<span data-ttu-id="62729-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62729-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62729-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62729-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62729-129">輸入</span><span class="sxs-lookup"><span data-stu-id="62729-129">INPUTS</span></span>

### <span data-ttu-id="62729-130">System.object</span><span class="sxs-lookup"><span data-stu-id="62729-130">System.String</span></span>

## <span data-ttu-id="62729-131">輸出</span><span class="sxs-lookup"><span data-stu-id="62729-131">OUTPUTS</span></span>

### <span data-ttu-id="62729-132">IntegrationAccount 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="62729-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="62729-133">筆記</span><span class="sxs-lookup"><span data-stu-id="62729-133">NOTES</span></span>

## <span data-ttu-id="62729-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="62729-134">RELATED LINKS</span></span>

[<span data-ttu-id="62729-135">AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="62729-135">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)

[<span data-ttu-id="62729-136">新-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="62729-136">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="62729-137">移除-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="62729-137">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="62729-138">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="62729-138">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


