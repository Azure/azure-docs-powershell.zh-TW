---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: e1e6efbdeaed90fe7591ed2dd5a645955dd5a314
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909462"
---
# <span data-ttu-id="c596f-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c596f-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="c596f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c596f-102">SYNOPSIS</span></span>
<span data-ttu-id="c596f-103">在指定的資源群組和群組下建立新的服務結構應用程式。</span><span class="sxs-lookup"><span data-stu-id="c596f-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="c596f-104">語法</span><span class="sxs-lookup"><span data-stu-id="c596f-104">SYNTAX</span></span>

### <span data-ttu-id="c596f-105">SkipAppTypeVersion (預設) </span><span class="sxs-lookup"><span data-stu-id="c596f-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c596f-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c596f-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c596f-107">描述</span><span class="sxs-lookup"><span data-stu-id="c596f-107">DESCRIPTION</span></span>
<span data-ttu-id="c596f-108">此 Cmdlet 會建立指定資源群組和群組下的新服務結構應用程式。</span><span class="sxs-lookup"><span data-stu-id="c596f-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="c596f-109">參數 -PackageUrl 可用來建立類型版本，如果類型版本已經離開，但其狀態為 '失敗'，Cmdlet 會詢問使用者是否要重新建立類型版本。</span><span class="sxs-lookup"><span data-stu-id="c596f-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="c596f-110">如果命令繼續以 "Failed" 狀態執行，該命令會停止程式並引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="c596f-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="c596f-111">例子</span><span class="sxs-lookup"><span data-stu-id="c596f-111">EXAMPLES</span></span>

### <span data-ttu-id="c596f-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="c596f-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="c596f-113">此範例在資源群組 "testRG" 和叢集 "testCluster" 下建立應用程式 "testApp"。</span><span class="sxs-lookup"><span data-stu-id="c596f-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="c596f-114">應用程式類型 "TestAppType" 版本 "v1" 應該已經存在於該組集中，而且應用程式參數應該在應用程式清單中定義，否則 Cmdlet 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="c596f-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="c596f-115">範例 2：在建立應用程式之前，指定 -PackageUrl 以建立應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="c596f-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="c596f-116">此範例會使用提供的套件 URL 建立應用程式類型 "TestAppType" 版本 "v1"。</span><span class="sxs-lookup"><span data-stu-id="c596f-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="c596f-117">之後，它會繼續一般程式來建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="c596f-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="c596f-118">如果應用程式類型版本已經離開，且設置狀態為'失敗」，系統會提示您決定是否要重新建立類型版本。</span><span class="sxs-lookup"><span data-stu-id="c596f-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="c596f-119">參數</span><span class="sxs-lookup"><span data-stu-id="c596f-119">PARAMETERS</span></span>

### <span data-ttu-id="c596f-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="c596f-120">-ApplicationParameter</span></span>
<span data-ttu-id="c596f-121">將應用程式參數指定為金鑰/值組。</span><span class="sxs-lookup"><span data-stu-id="c596f-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="c596f-122">這些參數必須存在於應用程式清單中。</span><span class="sxs-lookup"><span data-stu-id="c596f-122">These parameters must exist in the application manifest.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c596f-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="c596f-123">-ApplicationTypeName</span></span>
<span data-ttu-id="c596f-124">指定應用程式類型的名稱</span><span class="sxs-lookup"><span data-stu-id="c596f-124">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c596f-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="c596f-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="c596f-126">指定應用程式類型版本</span><span class="sxs-lookup"><span data-stu-id="c596f-126">Specify the application type version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c596f-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c596f-127">-ClusterName</span></span>
<span data-ttu-id="c596f-128">指定組名。</span><span class="sxs-lookup"><span data-stu-id="c596f-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c596f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c596f-129">-DefaultProfile</span></span>
<span data-ttu-id="c596f-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c596f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c596f-131">-強制</span><span class="sxs-lookup"><span data-stu-id="c596f-131">-Force</span></span>
<span data-ttu-id="c596f-132">繼續但不提示</span><span class="sxs-lookup"><span data-stu-id="c596f-132">Continue without prompts</span></span>

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

### <span data-ttu-id="c596f-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="c596f-133">-MaximumNodeCount</span></span>
<span data-ttu-id="c596f-134">指定要放置應用程式的節點數目上限</span><span class="sxs-lookup"><span data-stu-id="c596f-134">Specifies the maximum number of nodes on which to place an application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c596f-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="c596f-135">-MinimumNodeCount</span></span>
<span data-ttu-id="c596f-136">指定 Service 準備此應用程式容量的節點數目</span><span class="sxs-lookup"><span data-stu-id="c596f-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c596f-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="c596f-137">-Name</span></span>
<span data-ttu-id="c596f-138">指定應用程式的名稱</span><span class="sxs-lookup"><span data-stu-id="c596f-138">Specify the name of the application</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c596f-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="c596f-139">-PackageUrl</span></span>
<span data-ttu-id="c596f-140">指定應用程式套件 sfpkg 檔案的 URL</span><span class="sxs-lookup"><span data-stu-id="c596f-140">Specify the url of the application package sfpkg file</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAppTypeVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c596f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c596f-141">-ResourceGroupName</span></span>
<span data-ttu-id="c596f-142">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c596f-142">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c596f-143">-確認</span><span class="sxs-lookup"><span data-stu-id="c596f-143">-Confirm</span></span>
<span data-ttu-id="c596f-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c596f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c596f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c596f-145">-WhatIf</span></span>
<span data-ttu-id="c596f-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c596f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c596f-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c596f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c596f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c596f-148">CommonParameters</span></span>
<span data-ttu-id="c596f-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c596f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c596f-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c596f-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c596f-151">輸入</span><span class="sxs-lookup"><span data-stu-id="c596f-151">INPUTS</span></span>

### <span data-ttu-id="c596f-152">System.String</span><span class="sxs-lookup"><span data-stu-id="c596f-152">System.String</span></span>

### <span data-ttu-id="c596f-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c596f-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c596f-154">輸出</span><span class="sxs-lookup"><span data-stu-id="c596f-154">OUTPUTS</span></span>

### <span data-ttu-id="c596f-155">Microsoft.Azure.Commands.ServiceFabric.models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="c596f-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="c596f-156">筆記</span><span class="sxs-lookup"><span data-stu-id="c596f-156">NOTES</span></span>

## <span data-ttu-id="c596f-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="c596f-157">RELATED LINKS</span></span>
