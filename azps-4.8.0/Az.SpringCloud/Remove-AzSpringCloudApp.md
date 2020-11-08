---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/remove-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Remove-AzSpringCloudApp.md
ms.openlocfilehash: ace761bfd329c756baa27d1bff6300f2e030f377
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129870"
---
# <span data-ttu-id="43376-101">Remove-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="43376-101">Remove-AzSpringCloudApp</span></span>

## <span data-ttu-id="43376-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43376-102">SYNOPSIS</span></span>
<span data-ttu-id="43376-103">刪除應用程式的操作。</span><span class="sxs-lookup"><span data-stu-id="43376-103">Operation to delete an App.</span></span>

## <span data-ttu-id="43376-104">句法</span><span class="sxs-lookup"><span data-stu-id="43376-104">SYNTAX</span></span>

### <span data-ttu-id="43376-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="43376-105">Delete (Default)</span></span>
```
Remove-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="43376-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43376-106">DeleteViaIdentity</span></span>
```
Remove-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="43376-107">說明</span><span class="sxs-lookup"><span data-stu-id="43376-107">DESCRIPTION</span></span>
<span data-ttu-id="43376-108">刪除應用程式的操作。</span><span class="sxs-lookup"><span data-stu-id="43376-108">Operation to delete an App.</span></span>

## <span data-ttu-id="43376-109">示例</span><span class="sxs-lookup"><span data-stu-id="43376-109">EXAMPLES</span></span>

### <span data-ttu-id="43376-110">範例1：依名稱移除彈簧雲端 App。</span><span class="sxs-lookup"><span data-stu-id="43376-110">Example 1: Remove Spring Cloud App by name.</span></span>
```powershell
PS C:\> Remove-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
```

<span data-ttu-id="43376-111">依名稱移除彈簧雲端 App。</span><span class="sxs-lookup"><span data-stu-id="43376-111">Remove Spring Cloud App by name.</span></span>

### <span data-ttu-id="43376-112">範例2：從管道中移除彈簧雲端 App。</span><span class="sxs-lookup"><span data-stu-id="43376-112">Example 2: Remove Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Remove-AzSpringCloudApp
```

<span data-ttu-id="43376-113">從管道中移除彈簧雲端 App。</span><span class="sxs-lookup"><span data-stu-id="43376-113">Remove Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="43376-114">參數</span><span class="sxs-lookup"><span data-stu-id="43376-114">PARAMETERS</span></span>

### <span data-ttu-id="43376-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43376-115">-DefaultProfile</span></span>
<span data-ttu-id="43376-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="43376-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43376-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43376-117">-InputObject</span></span>
<span data-ttu-id="43376-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="43376-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43376-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="43376-119">-Name</span></span>
<span data-ttu-id="43376-120">App 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43376-120">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43376-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43376-121">-PassThru</span></span>
<span data-ttu-id="43376-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="43376-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="43376-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43376-123">-ResourceGroupName</span></span>
<span data-ttu-id="43376-124">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="43376-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="43376-125">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="43376-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="43376-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="43376-126">-ServiceName</span></span>
<span data-ttu-id="43376-127">服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43376-127">The name of the Service resource.</span></span>

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

### <span data-ttu-id="43376-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43376-128">-SubscriptionId</span></span>
<span data-ttu-id="43376-129">取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="43376-129">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="43376-130">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="43376-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="43376-131">-確認</span><span class="sxs-lookup"><span data-stu-id="43376-131">-Confirm</span></span>
<span data-ttu-id="43376-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="43376-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43376-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43376-133">-WhatIf</span></span>
<span data-ttu-id="43376-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43376-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43376-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43376-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43376-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43376-136">CommonParameters</span></span>
<span data-ttu-id="43376-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43376-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43376-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="43376-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43376-139">輸入</span><span class="sxs-lookup"><span data-stu-id="43376-139">INPUTS</span></span>

### <span data-ttu-id="43376-140">ISpringCloudIdentity （SpringCloud）的</span><span class="sxs-lookup"><span data-stu-id="43376-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="43376-141">輸出</span><span class="sxs-lookup"><span data-stu-id="43376-141">OUTPUTS</span></span>

### <span data-ttu-id="43376-142">System.object</span><span class="sxs-lookup"><span data-stu-id="43376-142">System.Boolean</span></span>

## <span data-ttu-id="43376-143">筆記</span><span class="sxs-lookup"><span data-stu-id="43376-143">NOTES</span></span>

<span data-ttu-id="43376-144">別名</span><span class="sxs-lookup"><span data-stu-id="43376-144">ALIASES</span></span>

<span data-ttu-id="43376-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="43376-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43376-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="43376-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43376-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="43376-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43376-148">INPUTOBJECT <ISpringCloudIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="43376-148">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43376-149">`[AppName <String>]`：應用程式資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43376-149">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="43376-150">`[BindingName <String>]`：系結資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43376-150">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="43376-151">`[CertificateName <String>]`：憑證資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43376-151">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="43376-152">`[DeploymentName <String>]`：部署資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43376-152">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="43376-153">`[DomainName <String>]`：自訂網域資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43376-153">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="43376-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="43376-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43376-155">`[Location <String>]`：區域</span><span class="sxs-lookup"><span data-stu-id="43376-155">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="43376-156">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="43376-156">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="43376-157">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="43376-157">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="43376-158">`[ServiceName <String>]`：服務資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="43376-158">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="43376-159">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="43376-159">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="43376-160">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="43376-160">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="43376-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="43376-161">RELATED LINKS</span></span>

