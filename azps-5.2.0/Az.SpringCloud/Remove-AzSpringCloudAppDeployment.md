---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 25b7b5c93f769982364a0df8f14f5fbe2f804fa2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276095"
---
# <span data-ttu-id="b540a-101">Remove-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="b540a-101">Remove-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="b540a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b540a-102">SYNOPSIS</span></span>
<span data-ttu-id="b540a-103">刪除部署的操作。</span><span class="sxs-lookup"><span data-stu-id="b540a-103">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="b540a-104">句法</span><span class="sxs-lookup"><span data-stu-id="b540a-104">SYNTAX</span></span>

### <span data-ttu-id="b540a-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="b540a-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b540a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b540a-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b540a-107">說明</span><span class="sxs-lookup"><span data-stu-id="b540a-107">DESCRIPTION</span></span>
<span data-ttu-id="b540a-108">刪除部署的操作。</span><span class="sxs-lookup"><span data-stu-id="b540a-108">Operation to delete a Deployment.</span></span>

## <span data-ttu-id="b540a-109">示例</span><span class="sxs-lookup"><span data-stu-id="b540a-109">EXAMPLES</span></span>

### <span data-ttu-id="b540a-110">範例1：依名稱移除彈簧雲端部署。</span><span class="sxs-lookup"><span data-stu-id="b540a-110">Example 1: Remove Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
```

<span data-ttu-id="b540a-111">依名稱移除彈簧雲端部署。</span><span class="sxs-lookup"><span data-stu-id="b540a-111">Remove Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="b540a-112">範例2：從管道中移除彈簧雲端部署。</span><span class="sxs-lookup"><span data-stu-id="b540a-112">Example 2: Remove Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Remove-AzSpringCloudAppDeployment
```

<span data-ttu-id="b540a-113">從管道中移除彈簧雲端部署。</span><span class="sxs-lookup"><span data-stu-id="b540a-113">Remove Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="b540a-114">參數</span><span class="sxs-lookup"><span data-stu-id="b540a-114">PARAMETERS</span></span>

### <span data-ttu-id="b540a-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="b540a-115">-AppName</span></span>
<span data-ttu-id="b540a-116">App 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b540a-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="b540a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b540a-117">-AsJob</span></span>
<span data-ttu-id="b540a-118">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="b540a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="b540a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b540a-119">-DefaultProfile</span></span>
<span data-ttu-id="b540a-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b540a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b540a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b540a-121">-InputObject</span></span>
<span data-ttu-id="b540a-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b540a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b540a-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="b540a-123">-Name</span></span>
<span data-ttu-id="b540a-124">部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b540a-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b540a-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b540a-125">-NoWait</span></span>
<span data-ttu-id="b540a-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="b540a-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b540a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b540a-127">-PassThru</span></span>
<span data-ttu-id="b540a-128">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="b540a-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b540a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b540a-129">-ResourceGroupName</span></span>
<span data-ttu-id="b540a-130">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b540a-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b540a-131">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="b540a-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b540a-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b540a-132">-ServiceName</span></span>
<span data-ttu-id="b540a-133">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b540a-133">The name of the Service resource.</span></span>

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

### <span data-ttu-id="b540a-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b540a-134">-SubscriptionId</span></span>
<span data-ttu-id="b540a-135">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="b540a-135">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b540a-136">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b540a-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b540a-137">-確認</span><span class="sxs-lookup"><span data-stu-id="b540a-137">-Confirm</span></span>
<span data-ttu-id="b540a-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b540a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b540a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b540a-139">-WhatIf</span></span>
<span data-ttu-id="b540a-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b540a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b540a-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b540a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b540a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b540a-142">CommonParameters</span></span>
<span data-ttu-id="b540a-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b540a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b540a-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b540a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b540a-145">輸入</span><span class="sxs-lookup"><span data-stu-id="b540a-145">INPUTS</span></span>

### <span data-ttu-id="b540a-146">ISpringCloudIdentity （SpringCloud）的</span><span class="sxs-lookup"><span data-stu-id="b540a-146">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="b540a-147">輸出</span><span class="sxs-lookup"><span data-stu-id="b540a-147">OUTPUTS</span></span>

### <span data-ttu-id="b540a-148">System.object</span><span class="sxs-lookup"><span data-stu-id="b540a-148">System.Boolean</span></span>

## <span data-ttu-id="b540a-149">筆記</span><span class="sxs-lookup"><span data-stu-id="b540a-149">NOTES</span></span>

<span data-ttu-id="b540a-150">別名</span><span class="sxs-lookup"><span data-stu-id="b540a-150">ALIASES</span></span>

<span data-ttu-id="b540a-151">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b540a-151">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b540a-152">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b540a-152">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b540a-153">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b540a-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b540a-154">INPUTOBJECT <ISpringCloudIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b540a-154">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b540a-155">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b540a-155">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="b540a-156">`[BindingName <String>]`：系結資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b540a-156">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="b540a-157">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b540a-157">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="b540a-158">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b540a-158">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="b540a-159">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b540a-159">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="b540a-160">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="b540a-160">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b540a-161">`[Location <String>]`：區域</span><span class="sxs-lookup"><span data-stu-id="b540a-161">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="b540a-162">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b540a-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b540a-163">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="b540a-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b540a-164">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b540a-164">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="b540a-165">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="b540a-165">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="b540a-166">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="b540a-166">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b540a-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="b540a-167">RELATED LINKS</span></span>

