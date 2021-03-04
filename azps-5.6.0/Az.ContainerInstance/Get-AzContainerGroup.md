---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/powershell/module/az.containerinstance/get-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Get-AzContainerGroup.md
ms.openlocfilehash: 65e6fbaa61285f946726fee9dce2261c998931cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916990"
---
# <span data-ttu-id="9c0f0-101">Get-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="9c0f0-101">Get-AzContainerGroup</span></span>

## <span data-ttu-id="9c0f0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9c0f0-102">SYNOPSIS</span></span>
<span data-ttu-id="9c0f0-103">獲得容器群組。</span><span class="sxs-lookup"><span data-stu-id="9c0f0-103">Gets container groups.</span></span>

## <span data-ttu-id="9c0f0-104">語法</span><span class="sxs-lookup"><span data-stu-id="9c0f0-104">SYNTAX</span></span>

### <span data-ttu-id="9c0f0-105">ListContainerGroupParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9c0f0-105">ListContainerGroupParamSet (Default)</span></span>
```
Get-AzContainerGroup [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c0f0-106">GetContainerGroupInResourceGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="9c0f0-106">GetContainerGroupInResourceGroupParamSet</span></span>
```
Get-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c0f0-107">GetContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="9c0f0-107">GetContainerGroupByResourceIdParamSet</span></span>
```
Get-AzContainerGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c0f0-108">描述</span><span class="sxs-lookup"><span data-stu-id="9c0f0-108">DESCRIPTION</span></span>
<span data-ttu-id="9c0f0-109">**Get-AzContainerGroup** Cmdlet 會取得指定的容器群組，或資源群組或訂閱中所有的容器群組。</span><span class="sxs-lookup"><span data-stu-id="9c0f0-109">The **Get-AzContainerGroup** cmdlet gets a specified container group or all the container groups in a resource group or the subscription.</span></span>

## <span data-ttu-id="9c0f0-110">例子</span><span class="sxs-lookup"><span data-stu-id="9c0f0-110">EXAMPLES</span></span>

### <span data-ttu-id="9c0f0-111">範例 1：獲得指定的容器群組</span><span class="sxs-lookup"><span data-stu-id="9c0f0-111">Example 1: Gets a specified container group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo -Name mycontainer

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="9c0f0-112">該命令會獲得指定的容器群組。</span><span class="sxs-lookup"><span data-stu-id="9c0f0-112">The command gets the specified container group.</span></span>

### <span data-ttu-id="9c0f0-113">範例 2：在資源群組中獲取容器群組</span><span class="sxs-lookup"><span data-stu-id="9c0f0-113">Example 2: Gets container groups in a resource group</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName demo

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo              container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo              container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="9c0f0-114">該命令會獲得資源群組中的容器群組 `demo` 。</span><span class="sxs-lookup"><span data-stu-id="9c0f0-114">The command gets the container groups in the resource group `demo`.</span></span>

### <span data-ttu-id="9c0f0-115">範例 3：在目前的訂閱中獲取容器群組</span><span class="sxs-lookup"><span data-stu-id="9c0f0-115">Example 3: Gets container groups in the current subscription</span></span>
```
PS C:\> Get-AzContainerGroup

ResourceGroupName Name                     Location   OsType  Image                         IP                   Resources        ProvisioningState
----------------- ----                     --------   ------  -----                         --                   ---------        -----------------
demo1             container1               west us    Linux   alpine:latest                 40.83.144.50:8002    1 cores/1 gb             Succeeded
demo2             container2               west us    Linux   alpine:latest                 104.42.228.253:8001  1 cores/1 gb             Succeeded
```

<span data-ttu-id="9c0f0-116">該命令會獲得目前訂閱中的容器群組。</span><span class="sxs-lookup"><span data-stu-id="9c0f0-116">The command gets the container groups in the current subscription.</span></span>

### <span data-ttu-id="9c0f0-117">範例 4：使用資源識別碼獲得容器群組。</span><span class="sxs-lookup"><span data-stu-id="9c0f0-117">Example 4: Gets container groups using resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals demo -ResourceNameEquals mycontainer | Get-AzContainerGroup

ResourceGroupName        : demo
Id                       : /subscriptions/ae43b1e3-c35d-4c8c-bc0d-f148b4c52b78/resourceGroups/demo/providers/Microsoft.ContainerInstance/containerGroups/mycontainer
Name                     : mycontainer
Type                     : Microsoft.ContainerInstance/containerGroups
Location                 : westus
Tags                     :
ProvisioningState        : Succeeded
Containers               : {mycontainer}
ImageRegistryCredentials :
RestartPolicy            :
IpAddress                : 13.88.10.240
Ports                    : {8000}
OsType                   : Linux
Volumes                  :
State                    : Running
Events                   : {}
```

<span data-ttu-id="9c0f0-118">該命令會獲得具有資源識別碼的容器群組。</span><span class="sxs-lookup"><span data-stu-id="9c0f0-118">The command gets the container group with the resource Id.</span></span>

## <span data-ttu-id="9c0f0-119">參數</span><span class="sxs-lookup"><span data-stu-id="9c0f0-119">PARAMETERS</span></span>

### <span data-ttu-id="9c0f0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c0f0-120">-DefaultProfile</span></span>
<span data-ttu-id="9c0f0-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c0f0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c0f0-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="9c0f0-122">-Name</span></span>
<span data-ttu-id="9c0f0-123">容器組名。</span><span class="sxs-lookup"><span data-stu-id="9c0f0-123">The container group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c0f0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c0f0-124">-ResourceGroupName</span></span>
<span data-ttu-id="9c0f0-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9c0f0-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListContainerGroupParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetContainerGroupInResourceGroupParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c0f0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c0f0-126">-ResourceId</span></span>
<span data-ttu-id="9c0f0-127">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9c0f0-127">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c0f0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c0f0-128">CommonParameters</span></span>
<span data-ttu-id="9c0f0-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9c0f0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c0f0-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9c0f0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c0f0-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9c0f0-131">INPUTS</span></span>

### <span data-ttu-id="9c0f0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9c0f0-132">System.String</span></span>

## <span data-ttu-id="9c0f0-133">輸出</span><span class="sxs-lookup"><span data-stu-id="9c0f0-133">OUTPUTS</span></span>

### <span data-ttu-id="9c0f0-134">Microsoft.Azure.Commands.ContainerInstance.models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="9c0f0-134">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="9c0f0-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9c0f0-135">NOTES</span></span>

## <span data-ttu-id="9c0f0-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c0f0-136">RELATED LINKS</span></span>
