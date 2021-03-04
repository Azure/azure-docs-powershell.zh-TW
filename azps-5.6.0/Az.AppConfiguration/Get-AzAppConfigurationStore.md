---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: e7f7c1f7493123793a32163b4e8f37bec8706e10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913981"
---
# <span data-ttu-id="24d74-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="24d74-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="24d74-102">簡介</span><span class="sxs-lookup"><span data-stu-id="24d74-102">SYNOPSIS</span></span>
<span data-ttu-id="24d74-103">取得或列出應用程式組配置存放區。</span><span class="sxs-lookup"><span data-stu-id="24d74-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="24d74-104">語法</span><span class="sxs-lookup"><span data-stu-id="24d74-104">SYNTAX</span></span>

### <span data-ttu-id="24d74-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="24d74-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="24d74-106">獲取</span><span class="sxs-lookup"><span data-stu-id="24d74-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="24d74-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="24d74-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="24d74-108">清單1</span><span class="sxs-lookup"><span data-stu-id="24d74-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="24d74-109">描述</span><span class="sxs-lookup"><span data-stu-id="24d74-109">DESCRIPTION</span></span>
<span data-ttu-id="24d74-110">取得或列出應用程式組配置存放區。</span><span class="sxs-lookup"><span data-stu-id="24d74-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="24d74-111">例子</span><span class="sxs-lookup"><span data-stu-id="24d74-111">EXAMPLES</span></span>

### <span data-ttu-id="24d74-112">範例 1：列出訂閱下的所有應用程式組配置存放區</span><span class="sxs-lookup"><span data-stu-id="24d74-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="24d74-113">此命令會列出訂閱下的所有應用程式組配置存放區。</span><span class="sxs-lookup"><span data-stu-id="24d74-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="24d74-114">範例 2：在資源群組下列出所有應用程式組配置存放區</span><span class="sxs-lookup"><span data-stu-id="24d74-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="24d74-115">此命令會列出資源群組下的所有應用程式組配置存放區。</span><span class="sxs-lookup"><span data-stu-id="24d74-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="24d74-116">範例 3：根據名稱取得應用程式組配置存放區</span><span class="sxs-lookup"><span data-stu-id="24d74-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="24d74-117">此命令會按名稱獲得應用程式組配置存放區。</span><span class="sxs-lookup"><span data-stu-id="24d74-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="24d74-118">範例 4：根據管線取得應用程式組配置存放區</span><span class="sxs-lookup"><span data-stu-id="24d74-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="24d74-119">此命令會按管線獲得應用程式組配置存放區。</span><span class="sxs-lookup"><span data-stu-id="24d74-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="24d74-120">參數</span><span class="sxs-lookup"><span data-stu-id="24d74-120">PARAMETERS</span></span>

### <span data-ttu-id="24d74-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d74-121">-DefaultProfile</span></span>
<span data-ttu-id="24d74-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="24d74-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24d74-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24d74-123">-InputObject</span></span>
<span data-ttu-id="24d74-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="24d74-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24d74-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="24d74-125">-Name</span></span>
<span data-ttu-id="24d74-126">組組存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="24d74-126">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d74-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d74-127">-ResourceGroupName</span></span>
<span data-ttu-id="24d74-128">容器註冊表所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="24d74-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d74-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24d74-129">-SubscriptionId</span></span>
<span data-ttu-id="24d74-130">Microsoft Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="24d74-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24d74-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d74-131">CommonParameters</span></span>
<span data-ttu-id="24d74-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="24d74-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d74-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24d74-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d74-134">輸入</span><span class="sxs-lookup"><span data-stu-id="24d74-134">INPUTS</span></span>

### <span data-ttu-id="24d74-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="24d74-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="24d74-136">輸出</span><span class="sxs-lookup"><span data-stu-id="24d74-136">OUTPUTS</span></span>

### <span data-ttu-id="24d74-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="24d74-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="24d74-138">筆記</span><span class="sxs-lookup"><span data-stu-id="24d74-138">NOTES</span></span>

<span data-ttu-id="24d74-139">別名</span><span class="sxs-lookup"><span data-stu-id="24d74-139">ALIASES</span></span>

<span data-ttu-id="24d74-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="24d74-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="24d74-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="24d74-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="24d74-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="24d74-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="24d74-143">INPUTOBJECT： <IAppConfigurationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="24d74-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="24d74-144">`[ConfigStoreName <String>]`：組組存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="24d74-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="24d74-145">`[GroupName <String>]`：私人連結資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="24d74-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="24d74-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="24d74-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="24d74-147">`[PrivateEndpointConnectionName <String>]`：私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="24d74-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="24d74-148">`[ResourceGroupName <String>]`：容器註冊表所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="24d74-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="24d74-149">`[SubscriptionId <String>]`：Microsoft Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="24d74-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="24d74-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="24d74-150">RELATED LINKS</span></span>

