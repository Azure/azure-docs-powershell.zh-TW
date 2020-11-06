---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: eaab02fe0e0adbd54bc80b15e6520442d9eb3c11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443924"
---
# <span data-ttu-id="d0463-101">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d0463-101">New-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="d0463-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0463-102">SYNOPSIS</span></span>
<span data-ttu-id="d0463-103">建立容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="d0463-103">Creates a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0463-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0463-104">SYNTAX</span></span>

### <span data-ttu-id="d0463-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d0463-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 -Location <String> [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0463-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0463-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0463-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0463-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0463-108">說明</span><span class="sxs-lookup"><span data-stu-id="d0463-108">DESCRIPTION</span></span>
<span data-ttu-id="d0463-109">New-AzureRmContainerRegistryReplication Cmdlet 會建立新的容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="d0463-109">The New-AzureRmContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="d0463-110">示例</span><span class="sxs-lookup"><span data-stu-id="d0463-110">EXAMPLES</span></span>

### <span data-ttu-id="d0463-111">範例1：建立新的容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="d0463-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="d0463-112">建立新的容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="d0463-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="d0463-113">參數</span><span class="sxs-lookup"><span data-stu-id="d0463-113">PARAMETERS</span></span>

### <span data-ttu-id="d0463-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0463-114">-DefaultProfile</span></span>
<span data-ttu-id="d0463-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0463-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0463-116">-位置</span><span class="sxs-lookup"><span data-stu-id="d0463-116">-Location</span></span>
<span data-ttu-id="d0463-117">容器登錄位置。</span><span class="sxs-lookup"><span data-stu-id="d0463-117">Container Registry Location.</span></span>
<span data-ttu-id="d0463-118">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="d0463-118">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0463-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0463-119">-Name</span></span>
<span data-ttu-id="d0463-120">容器登錄複製名稱。</span><span class="sxs-lookup"><span data-stu-id="d0463-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="d0463-121">預設為位置名稱。</span><span class="sxs-lookup"><span data-stu-id="d0463-121">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0463-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="d0463-122">-Registry</span></span>
<span data-ttu-id="d0463-123">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="d0463-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0463-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d0463-124">-RegistryName</span></span>
<span data-ttu-id="d0463-125">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="d0463-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0463-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0463-126">-ResourceGroupName</span></span>
<span data-ttu-id="d0463-127">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d0463-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0463-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0463-128">-ResourceId</span></span>
<span data-ttu-id="d0463-129">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d0463-129">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0463-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="d0463-130">-Tag</span></span>
<span data-ttu-id="d0463-131">容器登錄標記。</span><span class="sxs-lookup"><span data-stu-id="d0463-131">Container Registry Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0463-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d0463-132">-Confirm</span></span>
<span data-ttu-id="d0463-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d0463-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0463-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0463-134">-WhatIf</span></span>
<span data-ttu-id="d0463-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0463-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0463-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0463-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0463-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0463-137">CommonParameters</span></span>
<span data-ttu-id="d0463-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0463-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0463-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d0463-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0463-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d0463-140">INPUTS</span></span>

### <span data-ttu-id="d0463-141">System.object</span><span class="sxs-lookup"><span data-stu-id="d0463-141">System.String</span></span>

## <span data-ttu-id="d0463-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d0463-142">OUTPUTS</span></span>

### <span data-ttu-id="d0463-143">PSContainerRegistryReplication 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d0463-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="d0463-144">筆記</span><span class="sxs-lookup"><span data-stu-id="d0463-144">NOTES</span></span>

## <span data-ttu-id="d0463-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0463-145">RELATED LINKS</span></span>

[<span data-ttu-id="d0463-146">AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d0463-146">Get-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="d0463-147">移除-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="d0463-147">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
