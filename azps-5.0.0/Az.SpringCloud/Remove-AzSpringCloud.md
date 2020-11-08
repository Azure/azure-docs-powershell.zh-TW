---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloud.md
ms.openlocfilehash: 913011a9230b70c59b772eae306913c1e1e87432
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136675"
---
# <span data-ttu-id="cc796-101">Remove-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="cc796-101">Remove-AzSpringCloud</span></span>

## <span data-ttu-id="cc796-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc796-102">SYNOPSIS</span></span>
<span data-ttu-id="cc796-103">刪除服務的操作。</span><span class="sxs-lookup"><span data-stu-id="cc796-103">Operation to delete a Service.</span></span>

## <span data-ttu-id="cc796-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc796-104">SYNTAX</span></span>

### <span data-ttu-id="cc796-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="cc796-105">Delete (Default)</span></span>
```
Remove-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cc796-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cc796-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cc796-107">說明</span><span class="sxs-lookup"><span data-stu-id="cc796-107">DESCRIPTION</span></span>
<span data-ttu-id="cc796-108">刪除服務的操作。</span><span class="sxs-lookup"><span data-stu-id="cc796-108">Operation to delete a Service.</span></span>

## <span data-ttu-id="cc796-109">示例</span><span class="sxs-lookup"><span data-stu-id="cc796-109">EXAMPLES</span></span>

### <span data-ttu-id="cc796-110">範例1：依名稱移除彈簧雲端服務。</span><span class="sxs-lookup"><span data-stu-id="cc796-110">Example 1: Remove Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
```

<span data-ttu-id="cc796-111">依名稱移除彈簧雲端服務。</span><span class="sxs-lookup"><span data-stu-id="cc796-111">Remove Spring Cloud Service by name.</span></span>

### <span data-ttu-id="cc796-112">範例2：從管道中移除彈簧雲端服務。</span><span class="sxs-lookup"><span data-stu-id="cc796-112">Example 2: Remove Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Remove-AzSpringCloud
```

<span data-ttu-id="cc796-113">從管道中移除彈簧雲端服務。</span><span class="sxs-lookup"><span data-stu-id="cc796-113">Remove Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="cc796-114">參數</span><span class="sxs-lookup"><span data-stu-id="cc796-114">PARAMETERS</span></span>

### <span data-ttu-id="cc796-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc796-115">-AsJob</span></span>
<span data-ttu-id="cc796-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="cc796-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cc796-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc796-117">-DefaultProfile</span></span>
<span data-ttu-id="cc796-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc796-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc796-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc796-119">-InputObject</span></span>
<span data-ttu-id="cc796-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cc796-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc796-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc796-121">-Name</span></span>
<span data-ttu-id="cc796-122">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc796-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc796-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cc796-123">-NoWait</span></span>
<span data-ttu-id="cc796-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="cc796-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cc796-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc796-125">-PassThru</span></span>
<span data-ttu-id="cc796-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="cc796-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cc796-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc796-127">-ResourceGroupName</span></span>
<span data-ttu-id="cc796-128">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc796-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cc796-129">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="cc796-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc796-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc796-130">-SubscriptionId</span></span>
<span data-ttu-id="cc796-131">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="cc796-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cc796-132">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="cc796-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc796-133">-確認</span><span class="sxs-lookup"><span data-stu-id="cc796-133">-Confirm</span></span>
<span data-ttu-id="cc796-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cc796-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc796-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc796-135">-WhatIf</span></span>
<span data-ttu-id="cc796-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc796-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc796-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc796-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc796-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc796-138">CommonParameters</span></span>
<span data-ttu-id="cc796-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc796-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc796-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cc796-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc796-141">輸入</span><span class="sxs-lookup"><span data-stu-id="cc796-141">INPUTS</span></span>

### <span data-ttu-id="cc796-142">ISpringCloudIdentity （SpringCloud）的</span><span class="sxs-lookup"><span data-stu-id="cc796-142">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="cc796-143">輸出</span><span class="sxs-lookup"><span data-stu-id="cc796-143">OUTPUTS</span></span>

### <span data-ttu-id="cc796-144">System.object</span><span class="sxs-lookup"><span data-stu-id="cc796-144">System.Boolean</span></span>

## <span data-ttu-id="cc796-145">筆記</span><span class="sxs-lookup"><span data-stu-id="cc796-145">NOTES</span></span>

<span data-ttu-id="cc796-146">別名</span><span class="sxs-lookup"><span data-stu-id="cc796-146">ALIASES</span></span>

<span data-ttu-id="cc796-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="cc796-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cc796-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="cc796-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cc796-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="cc796-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cc796-150">INPUTOBJECT <ISpringCloudIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="cc796-150">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cc796-151">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc796-151">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="cc796-152">`[BindingName <String>]`：系結資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc796-152">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="cc796-153">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc796-153">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="cc796-154">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc796-154">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="cc796-155">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc796-155">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="cc796-156">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="cc796-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cc796-157">`[Location <String>]`：區域</span><span class="sxs-lookup"><span data-stu-id="cc796-157">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="cc796-158">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc796-158">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="cc796-159">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="cc796-159">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="cc796-160">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc796-160">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="cc796-161">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="cc796-161">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="cc796-162">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="cc796-162">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cc796-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc796-163">RELATED LINKS</span></span>

