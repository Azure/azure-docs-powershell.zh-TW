---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplication.md
ms.openlocfilehash: 5295caae4ffa0138a1c81fd08a5614f6e636eb41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287216"
---
# <span data-ttu-id="325b9-101">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="325b9-101">New-AzServiceFabricApplication</span></span>

## <span data-ttu-id="325b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="325b9-102">SYNOPSIS</span></span>
<span data-ttu-id="325b9-103">在指定的資源群組和群集底下建立新的服務結構應用程式。</span><span class="sxs-lookup"><span data-stu-id="325b9-103">Create new service fabric application under the specified resource group and cluster.</span></span>

## <span data-ttu-id="325b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="325b9-104">SYNTAX</span></span>

### <span data-ttu-id="325b9-105">SkipAppTypeVersion (預設) </span><span class="sxs-lookup"><span data-stu-id="325b9-105">SkipAppTypeVersion (Default)</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] [-MinimumNodeCount <Int64>] [-MaximumNodeCount <Int64>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="325b9-106">CreateAppTypeVersion</span><span class="sxs-lookup"><span data-stu-id="325b9-106">CreateAppTypeVersion</span></span>
```
New-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ApplicationTypeName] <String> [-ApplicationTypeVersion] <String> -Name <String>
 [-ApplicationParameter <Hashtable>] -PackageUrl <String> [-MinimumNodeCount <Int64>]
 [-MaximumNodeCount <Int64>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="325b9-107">說明</span><span class="sxs-lookup"><span data-stu-id="325b9-107">DESCRIPTION</span></span>
<span data-ttu-id="325b9-108">這個 Cmdlet 會在指定的資源群組和群集下建立新的服務結構應用程式。</span><span class="sxs-lookup"><span data-stu-id="325b9-108">This cmdlet creates a new service fabric application under the specified resource group and cluster.</span></span> <span data-ttu-id="325b9-109">PackageUrl 可以用來建立類型版本，如果類型版本已經存在，但其位於「失敗」狀態，則 Cmdlet 會詢問使用者是否要重新建立類型版本。</span><span class="sxs-lookup"><span data-stu-id="325b9-109">The parameter -PackageUrl can be used to create the type version, If the type version already exits but its in 'Failed' state the cmdlet will ask if the user wants to recreate the type version.</span></span> <span data-ttu-id="325b9-110">如果它繼續處於「失敗」狀態，則命令會停止程式並引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="325b9-110">If it continues in 'Failed' state, the command will stop the process and throw an exception.</span></span>

## <span data-ttu-id="325b9-111">示例</span><span class="sxs-lookup"><span data-stu-id="325b9-111">EXAMPLES</span></span>

### <span data-ttu-id="325b9-112">範例1</span><span class="sxs-lookup"><span data-stu-id="325b9-112">Example 1</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="325b9-113">這個範例會在 [資源] 群組的 [testRG] 和 [testCluster "群集中建立應用程式" testApp "。</span><span class="sxs-lookup"><span data-stu-id="325b9-113">This example creates the application "testApp" under resource group "testRG" and cluster "testCluster".</span></span> <span data-ttu-id="325b9-114">應用程式類型 "TestAppType" 版本 "v1" 應該已經存在於群集中，而且應該在應用程式資訊清單中定義應用程式參數，否則 Cmdlet 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="325b9-114">The application type "TestAppType" version "v1" should already exist in the cluster, and the application parameters should be defined in the application manifest otherwise the cmdlet will fail.</span></span>

### <span data-ttu-id="325b9-115">範例2：在建立應用程式之前，請先指定-PackageUrl 來建立應用程式類型版本。</span><span class="sxs-lookup"><span data-stu-id="325b9-115">Example 2: Specify -PackageUrl to create the application type version before creating the application.</span></span>
```powershell
PS C:\> New-AzServiceFabricApplication -ResourceGroupName "testRG" -ClusterName "testCluster" -ApplicationTypeName "TestAppType" -ApplicationTypeVersion "v1" -Name "testApp" -PackageUrl "https://sftestapp.blob.core.windows.net/sftestapp/testApp_1.0.sfpkg" -ApplicationParameter @{key0="value0";key1=$null;key2="value2"}
```

<span data-ttu-id="325b9-116">這個範例使用所提供的套件 url 來建立應用程式類型 "TestAppType" 版本 "v1"。</span><span class="sxs-lookup"><span data-stu-id="325b9-116">This example creates the application type "TestAppType"  version "v1" using the package url provided.</span></span> <span data-ttu-id="325b9-117">接著，它會繼續正常程式來建立應用程式。</span><span class="sxs-lookup"><span data-stu-id="325b9-117">After this, it will continue the normal process to create the application.</span></span> <span data-ttu-id="325b9-118">如果應用程式類型版本已經退出，且在「失敗」中進行提供，則會提示使用者是否要重新建立類型版本。</span><span class="sxs-lookup"><span data-stu-id="325b9-118">If the application type version already exits and the provisioning state its in 'Failed' it will prompt to decide if the user wants to recreate the type version.</span></span>

## <span data-ttu-id="325b9-119">參數</span><span class="sxs-lookup"><span data-stu-id="325b9-119">PARAMETERS</span></span>

### <span data-ttu-id="325b9-120">-ApplicationParameter</span><span class="sxs-lookup"><span data-stu-id="325b9-120">-ApplicationParameter</span></span>
<span data-ttu-id="325b9-121">將應用程式參數指定為鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="325b9-121">Specify the application parameters as key/value pairs.</span></span>
<span data-ttu-id="325b9-122">這些參數必須存在於應用程式資訊清單中。</span><span class="sxs-lookup"><span data-stu-id="325b9-122">These parameters must exist in the application manifest.</span></span>

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

### <span data-ttu-id="325b9-123">-ApplicationTypeName</span><span class="sxs-lookup"><span data-stu-id="325b9-123">-ApplicationTypeName</span></span>
<span data-ttu-id="325b9-124">指定應用程式類型的名稱</span><span class="sxs-lookup"><span data-stu-id="325b9-124">Specify the name of the application type</span></span>

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

### <span data-ttu-id="325b9-125">-ApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="325b9-125">-ApplicationTypeVersion</span></span>
<span data-ttu-id="325b9-126">指定應用程式類型版本</span><span class="sxs-lookup"><span data-stu-id="325b9-126">Specify the application type version</span></span>

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

### <span data-ttu-id="325b9-127">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="325b9-127">-ClusterName</span></span>
<span data-ttu-id="325b9-128">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="325b9-128">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="325b9-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="325b9-129">-DefaultProfile</span></span>
<span data-ttu-id="325b9-130">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="325b9-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="325b9-131">-Force</span><span class="sxs-lookup"><span data-stu-id="325b9-131">-Force</span></span>
<span data-ttu-id="325b9-132">繼續但不提示</span><span class="sxs-lookup"><span data-stu-id="325b9-132">Continue without prompts</span></span>

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

### <span data-ttu-id="325b9-133">-MaximumNodeCount</span><span class="sxs-lookup"><span data-stu-id="325b9-133">-MaximumNodeCount</span></span>
<span data-ttu-id="325b9-134">指定要放置應用程式的最大節點數</span><span class="sxs-lookup"><span data-stu-id="325b9-134">Specifies the maximum number of nodes on which to place an application</span></span>

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

### <span data-ttu-id="325b9-135">-MinimumNodeCount</span><span class="sxs-lookup"><span data-stu-id="325b9-135">-MinimumNodeCount</span></span>
<span data-ttu-id="325b9-136">指定服務結構將針對此應用程式保留容量的最小節點數</span><span class="sxs-lookup"><span data-stu-id="325b9-136">Specifies the minimum number of nodes where Service Fabric will reserve capacity for this application</span></span>

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

### <span data-ttu-id="325b9-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="325b9-137">-Name</span></span>
<span data-ttu-id="325b9-138">指定應用程式的名稱</span><span class="sxs-lookup"><span data-stu-id="325b9-138">Specify the name of the application</span></span>

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

### <span data-ttu-id="325b9-139">-PackageUrl</span><span class="sxs-lookup"><span data-stu-id="325b9-139">-PackageUrl</span></span>
<span data-ttu-id="325b9-140">指定應用程式套件 sfpkg 檔案的 url</span><span class="sxs-lookup"><span data-stu-id="325b9-140">Specify the url of the application package sfpkg file</span></span>

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

### <span data-ttu-id="325b9-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="325b9-141">-ResourceGroupName</span></span>
<span data-ttu-id="325b9-142">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="325b9-142">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="325b9-143">-確認</span><span class="sxs-lookup"><span data-stu-id="325b9-143">-Confirm</span></span>
<span data-ttu-id="325b9-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="325b9-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="325b9-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="325b9-145">-WhatIf</span></span>
<span data-ttu-id="325b9-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="325b9-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="325b9-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="325b9-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="325b9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325b9-148">CommonParameters</span></span>
<span data-ttu-id="325b9-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="325b9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="325b9-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="325b9-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325b9-151">輸入</span><span class="sxs-lookup"><span data-stu-id="325b9-151">INPUTS</span></span>

### <span data-ttu-id="325b9-152">System.object</span><span class="sxs-lookup"><span data-stu-id="325b9-152">System.String</span></span>

### <span data-ttu-id="325b9-153">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="325b9-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="325b9-154">輸出</span><span class="sxs-lookup"><span data-stu-id="325b9-154">OUTPUTS</span></span>

### <span data-ttu-id="325b9-155">PSApplication 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="325b9-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="325b9-156">筆記</span><span class="sxs-lookup"><span data-stu-id="325b9-156">NOTES</span></span>

## <span data-ttu-id="325b9-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="325b9-157">RELATED LINKS</span></span>
