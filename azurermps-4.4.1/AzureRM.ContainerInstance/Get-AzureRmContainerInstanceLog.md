---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Get-AzureRmContainerInstanceLog.md
ms.openlocfilehash: 8845d9b5ac5dba0a2170e3184c866c39be29b1b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453576"
---
# <span data-ttu-id="22faf-101">Get-AzureRmContainerInstanceLog</span><span class="sxs-lookup"><span data-stu-id="22faf-101">Get-AzureRmContainerInstanceLog</span></span>

## <span data-ttu-id="22faf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22faf-102">SYNOPSIS</span></span>
<span data-ttu-id="22faf-103">在容器群組中取得容器實例的記錄。</span><span class="sxs-lookup"><span data-stu-id="22faf-103">Get the logs of a container instance in a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22faf-104">句法</span><span class="sxs-lookup"><span data-stu-id="22faf-104">SYNTAX</span></span>

### <span data-ttu-id="22faf-105">GetContainerInstanceLogByNamesParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="22faf-105">GetContainerInstanceLogByNamesParamSet (Default)</span></span>
```
Get-AzureRmContainerInstanceLog [-ResourceGroupName] <String> -ContainerGroupName <String> [-Name <String>]
 [-Tail <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22faf-106">GetContainerInstanceLogByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="22faf-106">GetContainerInstanceLogByPSContainerGroupParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -InputContainerGroup <PSContainerGroup> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22faf-107">GetContainerInstanceLogByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="22faf-107">GetContainerInstanceLogByResourceIdParamSet</span></span>
```
Get-AzureRmContainerInstanceLog -ResourceId <String> [-Name <String>] [-Tail <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22faf-108">說明</span><span class="sxs-lookup"><span data-stu-id="22faf-108">DESCRIPTION</span></span>
<span data-ttu-id="22faf-109">**AzureRmContainerInstanceLog** Cmdlet 會取得容器群組中容器的記錄。</span><span class="sxs-lookup"><span data-stu-id="22faf-109">The **Get-AzureRmContainerInstanceLog** cmdlet gets the logs of a container in a container group.</span></span>

## <span data-ttu-id="22faf-110">示例</span><span class="sxs-lookup"><span data-stu-id="22faf-110">EXAMPLES</span></span>

### <span data-ttu-id="22faf-111">範例1：取得容器實例的尾部記錄</span><span class="sxs-lookup"><span data-stu-id="22faf-111">Example 1: Get the tail log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="22faf-112">從 `container1` 容器群組中取得記錄 `mycontainer` 。</span><span class="sxs-lookup"><span data-stu-id="22faf-112">Get the log from `container1` in container group `mycontainer`.</span></span> <span data-ttu-id="22faf-113">根據預設，它會傳回最多4MB 記錄內容。</span><span class="sxs-lookup"><span data-stu-id="22faf-113">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="22faf-114">範例2：取得容器實例的尾部記錄與容器群組的名稱相同</span><span class="sxs-lookup"><span data-stu-id="22faf-114">Example 2: Get the tail log of a container instance that has the same name as the container group</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="22faf-115">從 `mycontainer` 容器群組中取得記錄 `mycontainer` 。</span><span class="sxs-lookup"><span data-stu-id="22faf-115">Get the log from `mycontainer` in container group `mycontainer`.</span></span> <span data-ttu-id="22faf-116">根據預設，它會傳回最多4MB 記錄內容。</span><span class="sxs-lookup"><span data-stu-id="22faf-116">By default, it will return up to 4MB log content.</span></span>

### <span data-ttu-id="22faf-117">範例3：取得容器實例的結尾2行記錄</span><span class="sxs-lookup"><span data-stu-id="22faf-117">Example 3: Get the tail 2 lines of log of a container instance</span></span>
```
PS C:\> Get-AzureRmContainerInstanceLog -ResourceGroupName demo -ContainerGroupName mycontainer -Name container1 -Tail 2

Log line 3.
Log line 4.
```

<span data-ttu-id="22faf-118">從容器群組中取得尾部2行的記錄 `container1` `mycontainer` 。</span><span class="sxs-lookup"><span data-stu-id="22faf-118">Get the tail 2 lines of log from `container1` in container group `mycontainer`.</span></span>

### <span data-ttu-id="22faf-119">範例4：在容器群組中的管道中取得容器實例的尾部記錄</span><span class="sxs-lookup"><span data-stu-id="22faf-119">Example 4: Get the tail log of a container instance in a piped in container group</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName demo -Name mycontainer | Get-AzureRmContainerInstanceLog

Log line 1.
Log line 2.
Log line 3.
Log line 4.
```

<span data-ttu-id="22faf-120">從容器群組的管道中取得記錄 `mycontainer` `mycontainer` 。</span><span class="sxs-lookup"><span data-stu-id="22faf-120">Get the log from `mycontainer` in piped in container group `mycontainer`.</span></span> <span data-ttu-id="22faf-121">根據預設，它會傳回最多4MB 記錄內容。</span><span class="sxs-lookup"><span data-stu-id="22faf-121">By default, it will return up to 4MB log content.</span></span>

## <span data-ttu-id="22faf-122">參數</span><span class="sxs-lookup"><span data-stu-id="22faf-122">PARAMETERS</span></span>

### <span data-ttu-id="22faf-123">-ContainerGroupName</span><span class="sxs-lookup"><span data-stu-id="22faf-123">-ContainerGroupName</span></span>
<span data-ttu-id="22faf-124">容器組名。</span><span class="sxs-lookup"><span data-stu-id="22faf-124">The container group name.</span></span>

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

### <span data-ttu-id="22faf-125">-InputContainerGroup</span><span class="sxs-lookup"><span data-stu-id="22faf-125">-InputContainerGroup</span></span>
<span data-ttu-id="22faf-126">輸入容器群組物件。</span><span class="sxs-lookup"><span data-stu-id="22faf-126">The input container group object.</span></span>

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

### <span data-ttu-id="22faf-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="22faf-127">-Name</span></span>
<span data-ttu-id="22faf-128">容器群組中的容器實例名稱。</span><span class="sxs-lookup"><span data-stu-id="22faf-128">The container instance name in the container group.</span></span>
<span data-ttu-id="22faf-129">預設：與容器群組名稱相同</span><span class="sxs-lookup"><span data-stu-id="22faf-129">Default: the same as the container group name</span></span>

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

### <span data-ttu-id="22faf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22faf-130">-ResourceGroupName</span></span>
<span data-ttu-id="22faf-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="22faf-131">The resource group name.</span></span>

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

### <span data-ttu-id="22faf-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22faf-132">-ResourceId</span></span>
<span data-ttu-id="22faf-133">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="22faf-133">The resource id.</span></span>

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

### <span data-ttu-id="22faf-134">-尾</span><span class="sxs-lookup"><span data-stu-id="22faf-134">-Tail</span></span>
<span data-ttu-id="22faf-135">要將記錄結尾的行數。</span><span class="sxs-lookup"><span data-stu-id="22faf-135">The number of lines to tail the log.</span></span>
<span data-ttu-id="22faf-136">如果未指定，則 Cmdlet 會傳回最多4MB 的尾記錄</span><span class="sxs-lookup"><span data-stu-id="22faf-136">If not specify, the cmdlet will return up to 4MB tailed log</span></span>

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

### <span data-ttu-id="22faf-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22faf-137">-DefaultProfile</span></span>
<span data-ttu-id="22faf-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="22faf-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22faf-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22faf-139">CommonParameters</span></span>
<span data-ttu-id="22faf-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22faf-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22faf-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22faf-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22faf-142">輸入</span><span class="sxs-lookup"><span data-stu-id="22faf-142">INPUTS</span></span>

### <span data-ttu-id="22faf-143">PSContainerGroup 中的 ContainerInstance。</span><span class="sxs-lookup"><span data-stu-id="22faf-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="22faf-144">輸出</span><span class="sxs-lookup"><span data-stu-id="22faf-144">OUTPUTS</span></span>

### <span data-ttu-id="22faf-145">System.object</span><span class="sxs-lookup"><span data-stu-id="22faf-145">System.String</span></span>

## <span data-ttu-id="22faf-146">筆記</span><span class="sxs-lookup"><span data-stu-id="22faf-146">NOTES</span></span>

## <span data-ttu-id="22faf-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="22faf-147">RELATED LINKS</span></span>

