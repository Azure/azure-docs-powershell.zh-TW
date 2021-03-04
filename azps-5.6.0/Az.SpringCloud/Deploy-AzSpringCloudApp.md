---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: 96b3b3fcb2fcea50e1607c67d98079e5d1600f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902754"
---
# <span data-ttu-id="649db-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="649db-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="649db-102">簡介</span><span class="sxs-lookup"><span data-stu-id="649db-102">SYNOPSIS</span></span>
<span data-ttu-id="649db-103">將內建的罐子部署到服務中。</span><span class="sxs-lookup"><span data-stu-id="649db-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="649db-104">語法</span><span class="sxs-lookup"><span data-stu-id="649db-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="649db-105">描述</span><span class="sxs-lookup"><span data-stu-id="649db-105">DESCRIPTION</span></span>
<span data-ttu-id="649db-106">將內建的罐子部署到服務中。</span><span class="sxs-lookup"><span data-stu-id="649db-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="649db-107">例子</span><span class="sxs-lookup"><span data-stu-id="649db-107">EXAMPLES</span></span>

### <span data-ttu-id="649db-108">範例 1：根據名稱部署本地編譯的 jar 到服務。</span><span class="sxs-lookup"><span data-stu-id="649db-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="649db-109">根據名稱部署本地編譯的罐子到服務。</span><span class="sxs-lookup"><span data-stu-id="649db-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="649db-110">參數</span><span class="sxs-lookup"><span data-stu-id="649db-110">PARAMETERS</span></span>

### <span data-ttu-id="649db-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="649db-111">-AsJob</span></span>
<span data-ttu-id="649db-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="649db-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="649db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="649db-113">-DefaultProfile</span></span>
<span data-ttu-id="649db-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="649db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="649db-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="649db-115">-JarPath</span></span>
<span data-ttu-id="649db-116">罐子的路徑必須解說。</span><span class="sxs-lookup"><span data-stu-id="649db-116">The path of the jar need to be deploied.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="649db-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="649db-117">-Name</span></span>
<span data-ttu-id="649db-118">應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="649db-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="649db-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="649db-119">-NoWait</span></span>
<span data-ttu-id="649db-120">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="649db-120">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="649db-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="649db-121">-ResourceGroupName</span></span>
<span data-ttu-id="649db-122">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="649db-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="649db-123">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="649db-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="649db-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="649db-124">-ServiceName</span></span>
<span data-ttu-id="649db-125">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="649db-125">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="649db-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="649db-126">-SubscriptionId</span></span>
<span data-ttu-id="649db-127">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="649db-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="649db-128">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="649db-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="649db-129">-確認</span><span class="sxs-lookup"><span data-stu-id="649db-129">-Confirm</span></span>
<span data-ttu-id="649db-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="649db-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="649db-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="649db-131">-WhatIf</span></span>
<span data-ttu-id="649db-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="649db-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="649db-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="649db-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="649db-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="649db-134">CommonParameters</span></span>
<span data-ttu-id="649db-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="649db-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="649db-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="649db-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="649db-137">輸入</span><span class="sxs-lookup"><span data-stu-id="649db-137">INPUTS</span></span>

## <span data-ttu-id="649db-138">輸出</span><span class="sxs-lookup"><span data-stu-id="649db-138">OUTPUTS</span></span>

### <span data-ttu-id="649db-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="649db-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="649db-140">筆記</span><span class="sxs-lookup"><span data-stu-id="649db-140">NOTES</span></span>

<span data-ttu-id="649db-141">別名</span><span class="sxs-lookup"><span data-stu-id="649db-141">ALIASES</span></span>

## <span data-ttu-id="649db-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="649db-142">RELATED LINKS</span></span>

