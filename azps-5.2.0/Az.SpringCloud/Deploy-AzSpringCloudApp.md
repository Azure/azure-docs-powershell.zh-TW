---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: c6a7381c993b52995ab39a60fde54900092a5915
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280217"
---
# <span data-ttu-id="f05e4-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="f05e4-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="f05e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f05e4-102">SYNOPSIS</span></span>
<span data-ttu-id="f05e4-103">將建立的 jar 部署至服務。</span><span class="sxs-lookup"><span data-stu-id="f05e4-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="f05e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="f05e4-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f05e4-105">說明</span><span class="sxs-lookup"><span data-stu-id="f05e4-105">DESCRIPTION</span></span>
<span data-ttu-id="f05e4-106">將建立的 jar 部署至服務。</span><span class="sxs-lookup"><span data-stu-id="f05e4-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="f05e4-107">示例</span><span class="sxs-lookup"><span data-stu-id="f05e4-107">EXAMPLES</span></span>

### <span data-ttu-id="f05e4-108">範例1：依名稱將局部編譯的 jar 部署到服務。</span><span class="sxs-lookup"><span data-stu-id="f05e4-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="f05e4-109">依名稱將本機編譯的 jar 部署至服務。</span><span class="sxs-lookup"><span data-stu-id="f05e4-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="f05e4-110">參數</span><span class="sxs-lookup"><span data-stu-id="f05e4-110">PARAMETERS</span></span>

### <span data-ttu-id="f05e4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f05e4-111">-AsJob</span></span>
<span data-ttu-id="f05e4-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="f05e4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f05e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f05e4-113">-DefaultProfile</span></span>
<span data-ttu-id="f05e4-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f05e4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f05e4-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="f05e4-115">-JarPath</span></span>
<span data-ttu-id="f05e4-116">需要 deploied jar 的路徑。</span><span class="sxs-lookup"><span data-stu-id="f05e4-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="f05e4-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f05e4-117">-Name</span></span>
<span data-ttu-id="f05e4-118">App 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f05e4-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="f05e4-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f05e4-119">-NoWait</span></span>
<span data-ttu-id="f05e4-120">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="f05e4-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f05e4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f05e4-121">-ResourceGroupName</span></span>
<span data-ttu-id="f05e4-122">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f05e4-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f05e4-123">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="f05e4-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f05e4-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f05e4-124">-ServiceName</span></span>
<span data-ttu-id="f05e4-125">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f05e4-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="f05e4-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f05e4-126">-SubscriptionId</span></span>
<span data-ttu-id="f05e4-127">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="f05e4-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f05e4-128">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="f05e4-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f05e4-129">-確認</span><span class="sxs-lookup"><span data-stu-id="f05e4-129">-Confirm</span></span>
<span data-ttu-id="f05e4-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f05e4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f05e4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f05e4-131">-WhatIf</span></span>
<span data-ttu-id="f05e4-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f05e4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f05e4-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f05e4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f05e4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f05e4-134">CommonParameters</span></span>
<span data-ttu-id="f05e4-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f05e4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f05e4-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f05e4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f05e4-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f05e4-137">INPUTS</span></span>

## <span data-ttu-id="f05e4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="f05e4-138">OUTPUTS</span></span>

### <span data-ttu-id="f05e4-139">IAppResource （SpringCloud）。 Api20200701。</span><span class="sxs-lookup"><span data-stu-id="f05e4-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="f05e4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="f05e4-140">NOTES</span></span>

<span data-ttu-id="f05e4-141">別名</span><span class="sxs-lookup"><span data-stu-id="f05e4-141">ALIASES</span></span>

## <span data-ttu-id="f05e4-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f05e4-142">RELATED LINKS</span></span>

