---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 573dd2f4681ae140fbe98de5d9a7e9df4e2dc764
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448205"
---
# <span data-ttu-id="bb0ba-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="bb0ba-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="bb0ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb0ba-102">SYNOPSIS</span></span>
<span data-ttu-id="bb0ba-103">在現有的群集中新增節點類型。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb0ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb0ba-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb0ba-105">說明</span><span class="sxs-lookup"><span data-stu-id="bb0ba-105">DESCRIPTION</span></span>
<span data-ttu-id="bb0ba-106">在現有的群集中新增節點類型。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="bb0ba-107">示例</span><span class="sxs-lookup"><span data-stu-id="bb0ba-107">EXAMPLES</span></span>

### <span data-ttu-id="bb0ba-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bb0ba-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="bb0ba-109">這個命令會新增一個新的 NodeType "n2" （容量為5），而 vm 管理員名稱是 "adminName"。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="bb0ba-110">參數</span><span class="sxs-lookup"><span data-stu-id="bb0ba-110">PARAMETERS</span></span>

### <span data-ttu-id="bb0ba-111">-容量</span><span class="sxs-lookup"><span data-stu-id="bb0ba-111">-Capacity</span></span>
<span data-ttu-id="bb0ba-112">按需分配</span><span class="sxs-lookup"><span data-stu-id="bb0ba-112">Capacity</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb0ba-113">-DefaultProfile</span></span>
<span data-ttu-id="bb0ba-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb0ba-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="bb0ba-115">-DurabilityLevel</span></span>
<span data-ttu-id="bb0ba-116">指定 NodeType 的持久性層級。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases:
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ba-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="bb0ba-117">-Name</span></span>
<span data-ttu-id="bb0ba-118">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-118">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ba-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="bb0ba-119">-NodeType</span></span>
<span data-ttu-id="bb0ba-120">節點類型名稱。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-120">The node type name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ba-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb0ba-121">-ResourceGroupName</span></span>
<span data-ttu-id="bb0ba-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="bb0ba-123">層級</span><span class="sxs-lookup"><span data-stu-id="bb0ba-123">-Tier</span></span>
<span data-ttu-id="bb0ba-124">Vm Sku 層。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-124">Vm Sku Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ba-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="bb0ba-125">-VmPassword</span></span>
<span data-ttu-id="bb0ba-126">登入到 Vm 的密碼。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-126">The password of login to the Vm.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ba-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="bb0ba-127">-VmSku</span></span>
<span data-ttu-id="bb0ba-128">Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-128">The sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ba-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="bb0ba-129">-VmUserName</span></span>
<span data-ttu-id="bb0ba-130">登入到 Vm 的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-130">The user name for login to Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb0ba-131">-確認</span><span class="sxs-lookup"><span data-stu-id="bb0ba-131">-Confirm</span></span>
<span data-ttu-id="bb0ba-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb0ba-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb0ba-133">-WhatIf</span></span>
<span data-ttu-id="bb0ba-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb0ba-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb0ba-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb0ba-136">CommonParameters</span></span>
<span data-ttu-id="bb0ba-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb0ba-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb0ba-139">輸入</span><span class="sxs-lookup"><span data-stu-id="bb0ba-139">INPUTS</span></span>

### <span data-ttu-id="bb0ba-140">System.object</span><span class="sxs-lookup"><span data-stu-id="bb0ba-140">System.String</span></span>
<span data-ttu-id="bb0ba-141">參數： NodeType (ByValue) ，該級 (ByValue) ，VmSku (ByValue) ，VmUserName (ByValue) </span><span class="sxs-lookup"><span data-stu-id="bb0ba-141">Parameters: NodeType (ByValue), Tier (ByValue), VmSku (ByValue), VmUserName (ByValue)</span></span>

### <span data-ttu-id="bb0ba-142">System.object</span><span class="sxs-lookup"><span data-stu-id="bb0ba-142">System.Int32</span></span>
<span data-ttu-id="bb0ba-143">參數：容量 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="bb0ba-143">Parameters: Capacity (ByValue)</span></span>

### <span data-ttu-id="bb0ba-144">SecureString</span><span class="sxs-lookup"><span data-stu-id="bb0ba-144">System.Security.SecureString</span></span>
<span data-ttu-id="bb0ba-145">參數： VmPassword (ByValue) </span><span class="sxs-lookup"><span data-stu-id="bb0ba-145">Parameters: VmPassword (ByValue)</span></span>

### <span data-ttu-id="bb0ba-146">DurabilityLevel 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-146">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="bb0ba-147">參數： DurabilityLevel (ByValue) </span><span class="sxs-lookup"><span data-stu-id="bb0ba-147">Parameters: DurabilityLevel (ByValue)</span></span>

## <span data-ttu-id="bb0ba-148">輸出</span><span class="sxs-lookup"><span data-stu-id="bb0ba-148">OUTPUTS</span></span>

### <span data-ttu-id="bb0ba-149">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="bb0ba-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="bb0ba-150">筆記</span><span class="sxs-lookup"><span data-stu-id="bb0ba-150">NOTES</span></span>

## <span data-ttu-id="bb0ba-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb0ba-151">RELATED LINKS</span></span>
