---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: 8a80c323f1cf1d8d015faeda6541b77667a6ca19
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127316"
---
# <span data-ttu-id="9cf60-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="9cf60-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="9cf60-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9cf60-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf60-103">將建立的 jar 部署至服務。</span><span class="sxs-lookup"><span data-stu-id="9cf60-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="9cf60-104">句法</span><span class="sxs-lookup"><span data-stu-id="9cf60-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9cf60-105">說明</span><span class="sxs-lookup"><span data-stu-id="9cf60-105">DESCRIPTION</span></span>
<span data-ttu-id="9cf60-106">將建立的 jar 部署至服務。</span><span class="sxs-lookup"><span data-stu-id="9cf60-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="9cf60-107">示例</span><span class="sxs-lookup"><span data-stu-id="9cf60-107">EXAMPLES</span></span>

### <span data-ttu-id="9cf60-108">範例1：依名稱將局部編譯的 jar 部署到服務。</span><span class="sxs-lookup"><span data-stu-id="9cf60-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="9cf60-109">依名稱將本機編譯的 jar 部署至服務。</span><span class="sxs-lookup"><span data-stu-id="9cf60-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="9cf60-110">參數</span><span class="sxs-lookup"><span data-stu-id="9cf60-110">PARAMETERS</span></span>

### <span data-ttu-id="9cf60-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cf60-111">-AsJob</span></span>
<span data-ttu-id="9cf60-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="9cf60-112">Run the command as a job</span></span>

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

### <span data-ttu-id="9cf60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf60-113">-DefaultProfile</span></span>
<span data-ttu-id="9cf60-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9cf60-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cf60-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="9cf60-115">-JarPath</span></span>
<span data-ttu-id="9cf60-116">需要 deploied jar 的路徑。</span><span class="sxs-lookup"><span data-stu-id="9cf60-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="9cf60-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="9cf60-117">-Name</span></span>
<span data-ttu-id="9cf60-118">App 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cf60-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="9cf60-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9cf60-119">-NoWait</span></span>
<span data-ttu-id="9cf60-120">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="9cf60-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9cf60-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cf60-121">-ResourceGroupName</span></span>
<span data-ttu-id="9cf60-122">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cf60-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9cf60-123">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="9cf60-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9cf60-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9cf60-124">-ServiceName</span></span>
<span data-ttu-id="9cf60-125">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cf60-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="9cf60-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9cf60-126">-SubscriptionId</span></span>
<span data-ttu-id="9cf60-127">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="9cf60-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9cf60-128">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="9cf60-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9cf60-129">-確認</span><span class="sxs-lookup"><span data-stu-id="9cf60-129">-Confirm</span></span>
<span data-ttu-id="9cf60-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9cf60-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cf60-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cf60-131">-WhatIf</span></span>
<span data-ttu-id="9cf60-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9cf60-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cf60-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9cf60-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cf60-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf60-134">CommonParameters</span></span>
<span data-ttu-id="9cf60-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9cf60-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf60-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9cf60-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf60-137">輸入</span><span class="sxs-lookup"><span data-stu-id="9cf60-137">INPUTS</span></span>

## <span data-ttu-id="9cf60-138">輸出</span><span class="sxs-lookup"><span data-stu-id="9cf60-138">OUTPUTS</span></span>

### <span data-ttu-id="9cf60-139">IAppResource （SpringCloud）。 Api20190501Preview。</span><span class="sxs-lookup"><span data-stu-id="9cf60-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="9cf60-140">筆記</span><span class="sxs-lookup"><span data-stu-id="9cf60-140">NOTES</span></span>

<span data-ttu-id="9cf60-141">別名</span><span class="sxs-lookup"><span data-stu-id="9cf60-141">ALIASES</span></span>

## <span data-ttu-id="9cf60-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cf60-142">RELATED LINKS</span></span>

