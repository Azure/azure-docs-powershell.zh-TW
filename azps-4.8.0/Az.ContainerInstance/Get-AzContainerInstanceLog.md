---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/get-azcontainerinstancelog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerInstanceLog.md
ms.openlocfilehash: d279e5c08b43640d629e4146faf306d0e85482a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136082"
---
# <span data-ttu-id="dc867-101">Get-AzContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="dc867-101">Get-AzContainerInstanceLog</span></span>

## <span data-ttu-id="dc867-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc867-102">SYNOPSIS</span></span>
<span data-ttu-id="dc867-103">在容器群組中取得容器實例的記錄。</span><span class="sxs-lookup"><span data-stu-id="dc867-103">Get the logs of a container instance in a container group.</span></span>

## <span data-ttu-id="dc867-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc867-104">SYNTAX</span></span>

### <span data-ttu-id="dc867-105">GetContainerInstanceLogByNamesParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dc867-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc867-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="dc867-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc867-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="dc867-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc867-108">說明</span><span class="sxs-lookup"><span data-stu-id="dc867-108">DESCRIPTION</span></span>
<span data-ttu-id="dc867-109">**AzContainerInstanceLog** Cmdlet 會取得容器群組中容器的記錄。</span><span class="sxs-lookup"><span data-stu-id="dc867-109">The **Get-AzContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="dc867-110">示例</span><span class="sxs-lookup"><span data-stu-id="dc867-110">EXAMPLES</span></span>

### <span data-ttu-id="dc867-111">範例1：取得容器實例的尾部記錄</span><span class="sxs-lookup"><span data-stu-id="dc867-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="dc867-112">從 `container1` 容器群組中取得記錄 `mycontainer` 。</span><span class="sxs-lookup"><span data-stu-id="dc867-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="dc867-113">根據預設，它會傳回最多4MB 記錄內容。</span><span class="sxs-lookup"><span data-stu-id="dc867-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="dc867-114">範例2：取得容器實例的尾部記錄與容器群組的名稱相同</span><span class="sxs-lookup"><span data-stu-id="dc867-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="dc867-115">從 `mycontainer` 容器群組中取得記錄 `mycontainer` 。</span><span class="sxs-lookup"><span data-stu-id="dc867-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="dc867-116">根據預設，它會傳回最多4MB 記錄內容。</span><span class="sxs-lookup"><span data-stu-id="dc867-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="dc867-117">範例3：取得容器實例的結尾2行記錄</span><span class="sxs-lookup"><span data-stu-id="dc867-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="dc867-118">從容器群組中取得尾部2行的記錄 `container1` `mycontainer` 。</span><span class="sxs-lookup"><span data-stu-id="dc867-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="dc867-119">範例4：在容器群組中的管道中取得容器實例的尾部記錄</span><span class="sxs-lookup"><span data-stu-id="dc867-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="dc867-120">從容器群組的管道中取得記錄 `mycontainer` `mycontainer` 。</span><span class="sxs-lookup"><span data-stu-id="dc867-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="dc867-121">根據預設，它會傳回最多4MB 記錄內容。</span><span class="sxs-lookup"><span data-stu-id="dc867-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="dc867-122">參數</span><span class="sxs-lookup"><span data-stu-id="dc867-122">PARAMETERS</span></span>

### <span data-ttu-id="dc867-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="dc867-123">-ContainerGroupName</span></span>
<span data-ttu-id="dc867-124">容器組名。</span><span class="sxs-lookup"><span data-stu-id="dc867-124">The container group name.</span></span>

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

### <span data-ttu-id="dc867-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc867-125">-DefaultProfile</span></span>
<span data-ttu-id="dc867-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc867-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc867-127">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="dc867-127">-InputContainerGroup</span></span>
<span data-ttu-id="dc867-128">輸入容器群組物件。</span><span class="sxs-lookup"><span data-stu-id="dc867-128">The input container group object.</span></span>

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

### <span data-ttu-id="dc867-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc867-129">-Name</span></span>
<span data-ttu-id="dc867-130">容器群組中的容器實例名稱。</span><span class="sxs-lookup"><span data-stu-id="dc867-130">The container instance name in the container group.</span></span>
<span data-ttu-id="dc867-131">預設：與容器群組名稱相同</span><span class="sxs-lookup"><span data-stu-id="dc867-131">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="dc867-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc867-132">-ResourceGroupName</span></span>
<span data-ttu-id="dc867-133">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc867-133">The resource group name.</span></span>

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

### <span data-ttu-id="dc867-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc867-134">-ResourceId</span></span>
<span data-ttu-id="dc867-135">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="dc867-135">The resource id.</span></span>

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

### <span data-ttu-id="dc867-136">-尾</span><span class="sxs-lookup"><span data-stu-id="dc867-136">-Tail</span></span>
<span data-ttu-id="dc867-137">要將記錄結尾的行數。</span><span class="sxs-lookup"><span data-stu-id="dc867-137">The number of lines to tail the log.</span></span>
<span data-ttu-id="dc867-138">如果未指定，則 Cmdlet 會傳回最多4MB 的尾記錄</span><span class="sxs-lookup"><span data-stu-id="dc867-138">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="dc867-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc867-139">CommonParameters</span></span>
<span data-ttu-id="dc867-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc867-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc867-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc867-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc867-142">輸入</span><span class="sxs-lookup"><span data-stu-id="dc867-142">INPUTS</span></span>

### <span data-ttu-id="dc867-143">PSContainerGroup 中的 ContainerInstance。</span><span class="sxs-lookup"><span data-stu-id="dc867-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="dc867-144">System.object</span><span class="sxs-lookup"><span data-stu-id="dc867-144">System.String</span></span>

## <span data-ttu-id="dc867-145">輸出</span><span class="sxs-lookup"><span data-stu-id="dc867-145">OUTPUTS</span></span>

### <span data-ttu-id="dc867-146">System.object</span><span class="sxs-lookup"><span data-stu-id="dc867-146">System.String</span></span>

## <span data-ttu-id="dc867-147">筆記</span><span class="sxs-lookup"><span data-stu-id="dc867-147">NOTES</span></span>

## <span data-ttu-id="dc867-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc867-148">RELATED LINKS</span></span>