---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287584"
---
# <span data-ttu-id="9b5e5-101">Get-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="9b5e5-101">Get-AzAppConfigurationStore</span></span>

## <span data-ttu-id="9b5e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b5e5-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5e5-103">取得或列出 app 設定存放區。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-103">Get or list app configuration stores.</span></span>

## <span data-ttu-id="9b5e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b5e5-104">SYNTAX</span></span>

### <span data-ttu-id="9b5e5-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="9b5e5-105">List (Default)</span></span>
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9b5e5-106">獲取</span><span class="sxs-lookup"><span data-stu-id="9b5e5-106">Get</span></span>
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9b5e5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9b5e5-107">GetViaIdentity</span></span>
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b5e5-108">List1</span><span class="sxs-lookup"><span data-stu-id="9b5e5-108">List1</span></span>
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9b5e5-109">說明</span><span class="sxs-lookup"><span data-stu-id="9b5e5-109">DESCRIPTION</span></span>
<span data-ttu-id="9b5e5-110">取得或列出 app 設定存放區。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-110">Get or list app configuration stores.</span></span>

## <span data-ttu-id="9b5e5-111">示例</span><span class="sxs-lookup"><span data-stu-id="9b5e5-111">EXAMPLES</span></span>

### <span data-ttu-id="9b5e5-112">範例1：列出訂閱下的所有 app 設定儲存區</span><span class="sxs-lookup"><span data-stu-id="9b5e5-112">Example 1: List all app configuration stores under a subscription</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="9b5e5-113">這個命令會列出訂閱中的所有 app 設定儲存區。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-113">This command lists all app configuration stores under a subscription.</span></span>

### <span data-ttu-id="9b5e5-114">範例2：在 [資源] 群組下列出所有 app 設定的儲存區</span><span class="sxs-lookup"><span data-stu-id="9b5e5-114">Example 2: List all app configuration stores under a resource group</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="9b5e5-115">這個命令會列出 [資源] 群組底下的所有 app 設定存儲區。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-115">This command lists all app configuration stores under a resource group.</span></span>

### <span data-ttu-id="9b5e5-116">範例3：依名稱取得 app 設定儲存區</span><span class="sxs-lookup"><span data-stu-id="9b5e5-116">Example 3: Get an app configuration store by name</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="9b5e5-117">這個命令會透過名稱取得 app 設定儲存區。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-117">This command gets an app configuration store by name.</span></span>

### <span data-ttu-id="9b5e5-118">範例4：透過管線取得 app 設定儲存區</span><span class="sxs-lookup"><span data-stu-id="9b5e5-118">Example 4: Get an app configuration store by pipeline</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="9b5e5-119">這個命令會透過管線取得 app 配置存儲區。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-119">This command gets an app configuration store by pipeline.</span></span>

## <span data-ttu-id="9b5e5-120">參數</span><span class="sxs-lookup"><span data-stu-id="9b5e5-120">PARAMETERS</span></span>

### <span data-ttu-id="9b5e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5e5-121">-DefaultProfile</span></span>
<span data-ttu-id="9b5e5-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b5e5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b5e5-123">-InputObject</span></span>
<span data-ttu-id="9b5e5-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9b5e5-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b5e5-125">-Name</span></span>
<span data-ttu-id="9b5e5-126">配置存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-126">The name of the configuration store.</span></span>

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

### <span data-ttu-id="9b5e5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b5e5-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b5e5-128">容器註冊表所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="9b5e5-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b5e5-129">-SubscriptionId</span></span>
<span data-ttu-id="9b5e5-130">Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="9b5e5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5e5-131">CommonParameters</span></span>
<span data-ttu-id="9b5e5-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5e5-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5e5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="9b5e5-134">INPUTS</span></span>

### <span data-ttu-id="9b5e5-135">IAppConfigurationIdentity （AppConfiguration）的</span><span class="sxs-lookup"><span data-stu-id="9b5e5-135">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="9b5e5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="9b5e5-136">OUTPUTS</span></span>

### <span data-ttu-id="9b5e5-137">IConfigurationStore （AppConfiguration）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-137">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="9b5e5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="9b5e5-138">NOTES</span></span>

<span data-ttu-id="9b5e5-139">別名</span><span class="sxs-lookup"><span data-stu-id="9b5e5-139">ALIASES</span></span>

<span data-ttu-id="9b5e5-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9b5e5-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9b5e5-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9b5e5-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9b5e5-143">INPUTOBJECT <IAppConfigurationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="9b5e5-143">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9b5e5-144">`[ConfigStoreName <String>]`：配置存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-144">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="9b5e5-145">`[GroupName <String>]`：私人連結資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-145">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="9b5e5-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="9b5e5-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9b5e5-147">`[PrivateEndpointConnectionName <String>]`：私人端點連接名稱</span><span class="sxs-lookup"><span data-stu-id="9b5e5-147">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="9b5e5-148">`[ResourceGroupName <String>]`：容器註冊表所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-148">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="9b5e5-149">`[SubscriptionId <String>]`： Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="9b5e5-149">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="9b5e5-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b5e5-150">RELATED LINKS</span></span>

