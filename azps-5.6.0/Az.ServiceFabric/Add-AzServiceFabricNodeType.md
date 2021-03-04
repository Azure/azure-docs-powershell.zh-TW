---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNodeType.md
ms.openlocfilehash: aef628c121fa01cf07b0c70764b7d34ac10f259a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904313"
---
# <span data-ttu-id="88d80-101">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="88d80-101">Add-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="88d80-102">簡介</span><span class="sxs-lookup"><span data-stu-id="88d80-102">SYNOPSIS</span></span>
<span data-ttu-id="88d80-103">新增節點類型至現有組。</span><span class="sxs-lookup"><span data-stu-id="88d80-103">Add a new node type to the existing cluster.</span></span>

## <span data-ttu-id="88d80-104">語法</span><span class="sxs-lookup"><span data-stu-id="88d80-104">SYNTAX</span></span>

```
Add-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88d80-105">描述</span><span class="sxs-lookup"><span data-stu-id="88d80-105">DESCRIPTION</span></span>
<span data-ttu-id="88d80-106">新增節點類型至現有的組。</span><span class="sxs-lookup"><span data-stu-id="88d80-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="88d80-107">例子</span><span class="sxs-lookup"><span data-stu-id="88d80-107">EXAMPLES</span></span>

### <span data-ttu-id="88d80-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="88d80-108">Example 1</span></span>
```powershell
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="88d80-109">此命令會新增容量為 5 的新 NodeType 'n2，而 vm 系統管理員名稱為 'adminName'。</span><span class="sxs-lookup"><span data-stu-id="88d80-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="88d80-110">參數</span><span class="sxs-lookup"><span data-stu-id="88d80-110">PARAMETERS</span></span>

### <span data-ttu-id="88d80-111">-容量</span><span class="sxs-lookup"><span data-stu-id="88d80-111">-Capacity</span></span>
<span data-ttu-id="88d80-112">能力</span><span class="sxs-lookup"><span data-stu-id="88d80-112">Capacity</span></span>

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

### <span data-ttu-id="88d80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88d80-113">-DefaultProfile</span></span>
<span data-ttu-id="88d80-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="88d80-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88d80-115">-LevelyLevel</span><span class="sxs-lookup"><span data-stu-id="88d80-115">-DurabilityLevel</span></span>
<span data-ttu-id="88d80-116">指定 NodeType 的上線層級。</span><span class="sxs-lookup"><span data-stu-id="88d80-116">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="88d80-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="88d80-117">-Name</span></span>
<span data-ttu-id="88d80-118">指定組名</span><span class="sxs-lookup"><span data-stu-id="88d80-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="88d80-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="88d80-119">-NodeType</span></span>
<span data-ttu-id="88d80-120">節點類型名稱</span><span class="sxs-lookup"><span data-stu-id="88d80-120">The node type name</span></span>

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

### <span data-ttu-id="88d80-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88d80-121">-ResourceGroupName</span></span>
<span data-ttu-id="88d80-122">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="88d80-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="88d80-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="88d80-123">-Tier</span></span>
<span data-ttu-id="88d80-124">Vm Sku Tier</span><span class="sxs-lookup"><span data-stu-id="88d80-124">Vm Sku Tier</span></span>

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

### <span data-ttu-id="88d80-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="88d80-125">-VmPassword</span></span>
<span data-ttu-id="88d80-126">登入 Vm 的密碼</span><span class="sxs-lookup"><span data-stu-id="88d80-126">The password for login to the Vm</span></span>

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

### <span data-ttu-id="88d80-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="88d80-127">-VmSku</span></span>
<span data-ttu-id="88d80-128">SKU 名稱</span><span class="sxs-lookup"><span data-stu-id="88d80-128">The sku name</span></span>

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

### <span data-ttu-id="88d80-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="88d80-129">-VmUserName</span></span>
<span data-ttu-id="88d80-130">記錄到 Vm 的使用者名稱</span><span class="sxs-lookup"><span data-stu-id="88d80-130">The user name for logging to Vm</span></span>

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

### <span data-ttu-id="88d80-131">-確認</span><span class="sxs-lookup"><span data-stu-id="88d80-131">-Confirm</span></span>
<span data-ttu-id="88d80-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="88d80-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88d80-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88d80-133">-WhatIf</span></span>
<span data-ttu-id="88d80-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="88d80-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88d80-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="88d80-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88d80-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d80-136">CommonParameters</span></span>
<span data-ttu-id="88d80-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="88d80-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d80-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88d80-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d80-139">輸入</span><span class="sxs-lookup"><span data-stu-id="88d80-139">INPUTS</span></span>

### <span data-ttu-id="88d80-140">System.String</span><span class="sxs-lookup"><span data-stu-id="88d80-140">System.String</span></span>

### <span data-ttu-id="88d80-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="88d80-141">System.Int32</span></span>

### <span data-ttu-id="88d80-142">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="88d80-142">System.Security.SecureString</span></span>

### <span data-ttu-id="88d80-143">Microsoft.Azure.Commands.ServiceFabric.models.LevelyLevel</span><span class="sxs-lookup"><span data-stu-id="88d80-143">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="88d80-144">輸出</span><span class="sxs-lookup"><span data-stu-id="88d80-144">OUTPUTS</span></span>

### <span data-ttu-id="88d80-145">Microsoft.Azure.Commands.ServiceFabric.models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="88d80-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="88d80-146">筆記</span><span class="sxs-lookup"><span data-stu-id="88d80-146">NOTES</span></span>

## <span data-ttu-id="88d80-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="88d80-147">RELATED LINKS</span></span>
