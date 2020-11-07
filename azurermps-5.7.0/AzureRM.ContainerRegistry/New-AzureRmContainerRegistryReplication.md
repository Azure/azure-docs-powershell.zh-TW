---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 31170e24e88f6ce25c9fd344d254189eeeae64f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624190"
---
# <span data-ttu-id="ba7e2-101">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ba7e2-101">New-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="ba7e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba7e2-102">SYNOPSIS</span></span>
<span data-ttu-id="ba7e2-103">建立容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-103">Creates a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba7e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba7e2-104">SYNTAX</span></span>

### <span data-ttu-id="ba7e2-105">NameResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ba7e2-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 -Location <String> [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba7e2-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba7e2-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba7e2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba7e2-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba7e2-108">說明</span><span class="sxs-lookup"><span data-stu-id="ba7e2-108">DESCRIPTION</span></span>
<span data-ttu-id="ba7e2-109">New-AzureRmContainerRegistryReplication Cmdlet 會建立新的容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-109">The New-AzureRmContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="ba7e2-110">示例</span><span class="sxs-lookup"><span data-stu-id="ba7e2-110">EXAMPLES</span></span>

### <span data-ttu-id="ba7e2-111">範例1：建立新的容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="ba7e2-112">建立新的容器註冊複製。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="ba7e2-113">參數</span><span class="sxs-lookup"><span data-stu-id="ba7e2-113">PARAMETERS</span></span>

### <span data-ttu-id="ba7e2-114">-確認</span><span class="sxs-lookup"><span data-stu-id="ba7e2-114">-Confirm</span></span>
<span data-ttu-id="ba7e2-115">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba7e2-116">-DefaultProfile</span></span>
<span data-ttu-id="ba7e2-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7e2-118">-位置</span><span class="sxs-lookup"><span data-stu-id="ba7e2-118">-Location</span></span>
<span data-ttu-id="ba7e2-119">容器登錄位置。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-119">Container Registry Location.</span></span>
<span data-ttu-id="ba7e2-120">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-120">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7e2-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba7e2-121">-Name</span></span>
<span data-ttu-id="ba7e2-122">容器登錄複製名稱。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-122">Container Registry Replication Name.</span></span>
<span data-ttu-id="ba7e2-123">預設為位置名稱。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-123">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7e2-124">-Registry</span><span class="sxs-lookup"><span data-stu-id="ba7e2-124">-Registry</span></span>
<span data-ttu-id="ba7e2-125">分枝 Registry 物件。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-125">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7e2-126">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="ba7e2-126">-RegistryName</span></span>
<span data-ttu-id="ba7e2-127">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-127">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7e2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba7e2-128">-ResourceGroupName</span></span>
<span data-ttu-id="ba7e2-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7e2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba7e2-130">-ResourceId</span></span>
<span data-ttu-id="ba7e2-131">容器登錄資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ba7e2-131">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba7e2-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="ba7e2-132">-Tag</span></span>
<span data-ttu-id="ba7e2-133">容器登錄標記。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-133">Container Registry Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7e2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba7e2-134">-WhatIf</span></span>
<span data-ttu-id="ba7e2-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba7e2-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba7e2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba7e2-137">CommonParameters</span></span>
<span data-ttu-id="ba7e2-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba7e2-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba7e2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba7e2-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ba7e2-140">INPUTS</span></span>

### <span data-ttu-id="ba7e2-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ba7e2-141">System.String</span></span>

## <span data-ttu-id="ba7e2-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ba7e2-142">OUTPUTS</span></span>

### <span data-ttu-id="ba7e2-143">PSContainerRegistryReplication 中的 ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ba7e2-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="ba7e2-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ba7e2-144">NOTES</span></span>

## <span data-ttu-id="ba7e2-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba7e2-145">RELATED LINKS</span></span>

[<span data-ttu-id="ba7e2-146">AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ba7e2-146">Get-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="ba7e2-147">移除-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="ba7e2-147">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
