---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: de512f636b0a326029981e199b13926a9fc5824a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127321"
---
# <span data-ttu-id="1c9e8-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="1c9e8-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="1c9e8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c9e8-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9e8-103">在現有的群集中新增節點類型。</span><span class="sxs-lookup"><span data-stu-id="1c9e8-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="1c9e8-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c9e8-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c9e8-105">說明</span><span class="sxs-lookup"><span data-stu-id="1c9e8-105">DESCRIPTION</span></span>
<span data-ttu-id="1c9e8-106">在現有的群集中新增節點類型。</span><span class="sxs-lookup"><span data-stu-id="1c9e8-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="1c9e8-107">示例</span><span class="sxs-lookup"><span data-stu-id="1c9e8-107">EXAMPLES</span></span>

### <span data-ttu-id="1c9e8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1c9e8-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="1c9e8-109">這個命令會新增一個新的 NodeType "n2" （容量為5），而 vm 管理員名稱是 "adminName"。</span><span class="sxs-lookup"><span data-stu-id="1c9e8-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="1c9e8-110">參數</span><span class="sxs-lookup"><span data-stu-id="1c9e8-110">PARAMETERS</span></span>

### <span data-ttu-id="1c9e8-111">-容量</span><span class="sxs-lookup"><span data-stu-id="1c9e8-111">-Capacity</span></span>
<span data-ttu-id="1c9e8-112">按需分配</span><span class="sxs-lookup"><span data-stu-id="1c9e8-112">Capacity</span></span>

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

### <span data-ttu-id="1c9e8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9e8-113">-DefaultProfile</span></span>
<span data-ttu-id="1c9e8-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c9e8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c9e8-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="1c9e8-115">-DurabilityLevel</span></span>
<span data-ttu-id="1c9e8-116">指定 NodeType 的持久性層級。</span><span class="sxs-lookup"><span data-stu-id="1c9e8-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="1c9e8-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c9e8-117">-Name</span></span>
<span data-ttu-id="1c9e8-118">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="1c9e8-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="1c9e8-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="1c9e8-119">-NodeType</span></span>
<span data-ttu-id="1c9e8-120">節點類型名稱</span><span class="sxs-lookup"><span data-stu-id="1c9e8-120">The node type name</span></span>

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

### <span data-ttu-id="1c9e8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c9e8-121">-ResourceGroupName</span></span>
<span data-ttu-id="1c9e8-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c9e8-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="1c9e8-123">層級</span><span class="sxs-lookup"><span data-stu-id="1c9e8-123">-Tier</span></span>
<span data-ttu-id="1c9e8-124">Vm Sku 層級</span><span class="sxs-lookup"><span data-stu-id="1c9e8-124">Vm Sku Tier</span></span>

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

### <span data-ttu-id="1c9e8-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="1c9e8-125">-VmPassword</span></span>
<span data-ttu-id="1c9e8-126">登入到 Vm 的密碼</span><span class="sxs-lookup"><span data-stu-id="1c9e8-126">The password for login to the Vm</span></span>

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

### <span data-ttu-id="1c9e8-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="1c9e8-127">-VmSku</span></span>
<span data-ttu-id="1c9e8-128">Sku 名稱</span><span class="sxs-lookup"><span data-stu-id="1c9e8-128">The sku name</span></span>

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

### <span data-ttu-id="1c9e8-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="1c9e8-129">-VmUserName</span></span>
<span data-ttu-id="1c9e8-130">用於記錄到 Vm 的使用者名稱</span><span class="sxs-lookup"><span data-stu-id="1c9e8-130">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="1c9e8-131">-確認</span><span class="sxs-lookup"><span data-stu-id="1c9e8-131">-Confirm</span></span>
<span data-ttu-id="1c9e8-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1c9e8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c9e8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c9e8-133">-WhatIf</span></span>
<span data-ttu-id="1c9e8-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1c9e8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c9e8-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1c9e8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c9e8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9e8-136">CommonParameters</span></span>
<span data-ttu-id="1c9e8-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c9e8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9e8-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1c9e8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9e8-139">輸入</span><span class="sxs-lookup"><span data-stu-id="1c9e8-139">INPUTS</span></span>

### <span data-ttu-id="1c9e8-140">System.object</span><span class="sxs-lookup"><span data-stu-id="1c9e8-140">System.String</span></span>

### <span data-ttu-id="1c9e8-141">System.object</span><span class="sxs-lookup"><span data-stu-id="1c9e8-141">System.Int32</span></span>

### <span data-ttu-id="1c9e8-142">SecureString</span><span class="sxs-lookup"><span data-stu-id="1c9e8-142">System.Security.SecureString</span></span>

### <span data-ttu-id="1c9e8-143">DurabilityLevel 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="1c9e8-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="1c9e8-144">輸出</span><span class="sxs-lookup"><span data-stu-id="1c9e8-144">OUTPUTS</span></span>

### <span data-ttu-id="1c9e8-145">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="1c9e8-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="1c9e8-146">筆記</span><span class="sxs-lookup"><span data-stu-id="1c9e8-146">NOTES</span></span>

## <span data-ttu-id="1c9e8-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c9e8-147">RELATED LINKS</span></span>
