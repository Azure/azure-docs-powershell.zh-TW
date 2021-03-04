---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: 2ab0102534a8773ca1ca206bde2075e2bd7930f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916986"
---
# <span data-ttu-id="5bb7b-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="5bb7b-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="5bb7b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5bb7b-102">SYNOPSIS</span></span>
<span data-ttu-id="5bb7b-103">取得容器群組中容器實例的記錄。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="5bb7b-104">語法</span><span class="sxs-lookup"><span data-stu-id="5bb7b-104">SYNTAX</span></span>

### <span data-ttu-id="5bb7b-105">GetContainerInstanceLogByNamesParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5bb7b-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bb7b-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="5bb7b-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bb7b-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="5bb7b-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bb7b-108">描述</span><span class="sxs-lookup"><span data-stu-id="5bb7b-108">DESCRIPTION</span></span>
<span data-ttu-id="5bb7b-109">**Get-AzContainerInstanceLog** Cmdlet 會取得容器群組中容器的記錄。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="5bb7b-110">例子</span><span class="sxs-lookup"><span data-stu-id="5bb7b-110">EXAMPLES</span></span>

### <span data-ttu-id="5bb7b-111">範例 1：取得容器實例的尾數記錄</span><span class="sxs-lookup"><span data-stu-id="5bb7b-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="5bb7b-112">從容器群組 `container1` 取得記錄 `mycontainer` 。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="5bb7b-113">根據預設，它最多會返回 4 MB 記錄內容。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="5bb7b-114">範例 2：取得與容器群組名稱相同的容器實例尾數</span><span class="sxs-lookup"><span data-stu-id="5bb7b-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="5bb7b-115">從容器群組 `mycontainer` 取得記錄 `mycontainer` 。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="5bb7b-116">根據預設，它最多會返回 4 MB 記錄內容。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="5bb7b-117">範例 3：取得容器實例的結尾 2 行記錄</span><span class="sxs-lookup"><span data-stu-id="5bb7b-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="5bb7b-118">在容器群組中取得結尾 2 `container1` 行記錄 `mycontainer` 。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="5bb7b-119">範例 4：取得容器群組中管道中容器實例的尾端記錄</span><span class="sxs-lookup"><span data-stu-id="5bb7b-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="5bb7b-120">從容器群組 `mycontainer` 中的管道取得記錄 `mycontainer` 。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="5bb7b-121">根據預設，它最多會返回 4 MB 記錄內容。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="5bb7b-122">參數</span><span class="sxs-lookup"><span data-stu-id="5bb7b-122">PARAMETERS</span></span>

### <span data-ttu-id="5bb7b-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="5bb7b-123">-ContainerGroupName</span></span>
<span data-ttu-id="5bb7b-124">容器組名。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-124">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb7b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bb7b-125">-DefaultProfile</span></span>
<span data-ttu-id="5bb7b-126">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5bb7b-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="5bb7b-127">-InputContainerGroup</span></span>
<span data-ttu-id="5bb7b-128">輸入容器群組物件。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-128">The input container group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: GetContainerInstanceLogByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb7b-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="5bb7b-129">-Name</span></span>
<span data-ttu-id="5bb7b-130">容器群組中的容器實例名稱。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-130">The container instance name in the container group.</span></span>
<span data-ttu-id="5bb7b-131">預設：與容器組名相同</span><span class="sxs-lookup"><span data-stu-id="5bb7b-131">Default: the same as the container group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb7b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bb7b-132">-ResourceGroupName</span></span>
<span data-ttu-id="5bb7b-133">資源組名。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByNamesParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb7b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bb7b-134">-ResourceId</span></span>
<span data-ttu-id="5bb7b-135">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerInstanceLogByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5bb7b-136">-Tail</span><span class="sxs-lookup"><span data-stu-id="5bb7b-136">-Tail</span></span>
<span data-ttu-id="5bb7b-137">這是記錄結尾的行數。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="5bb7b-138">如果未指定，Cmdlet 會返回最多 4 MB 尾數的記錄</span><span class="sxs-lookup"><span data-stu-id="5bb7b-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb7b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bb7b-139">CommonParameters</span></span>
<span data-ttu-id="5bb7b-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bb7b-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="5bb7b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bb7b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="5bb7b-142">INPUTS</span></span>

### <span data-ttu-id="5bb7b-143">Microsoft.Azure.Commands.ContainerInstance.models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="5bb7b-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="5bb7b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5bb7b-144">System.String</span></span>

## <span data-ttu-id="5bb7b-145">輸出</span><span class="sxs-lookup"><span data-stu-id="5bb7b-145">OUTPUTS</span></span>

### <span data-ttu-id="5bb7b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="5bb7b-146">System.String</span></span>

## <span data-ttu-id="5bb7b-147">筆記</span><span class="sxs-lookup"><span data-stu-id="5bb7b-147">NOTES</span></span>

## <span data-ttu-id="5bb7b-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bb7b-148">RELATED LINKS</span></span>
