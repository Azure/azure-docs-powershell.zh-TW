---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 305e406a3f2ef723eb0431b495106bb688ffe61c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452347"
---
# <span data-ttu-id="e50f6-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="e50f6-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="e50f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e50f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e50f6-103">在現有的群集中新增節點類型。</span><span class="sxs-lookup"><span data-stu-id="e50f6-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e50f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="e50f6-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -Capacity <Int32> -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e50f6-105">說明</span><span class="sxs-lookup"><span data-stu-id="e50f6-105">DESCRIPTION</span></span>
<span data-ttu-id="e50f6-106">在現有的群集中新增節點類型。</span><span class="sxs-lookup"><span data-stu-id="e50f6-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="e50f6-107">示例</span><span class="sxs-lookup"><span data-stu-id="e50f6-107">EXAMPLES</span></span>

### <span data-ttu-id="e50f6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e50f6-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="e50f6-109">這個命令會新增一個新的 NodeType "n2" （容量為5），而 vm 管理員名稱是 "adminName"。</span><span class="sxs-lookup"><span data-stu-id="e50f6-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="e50f6-110">參數</span><span class="sxs-lookup"><span data-stu-id="e50f6-110">PARAMETERS</span></span>

### <span data-ttu-id="e50f6-111">-容量</span><span class="sxs-lookup"><span data-stu-id="e50f6-111">-Capacity</span></span>
<span data-ttu-id="e50f6-112">按需分配</span><span class="sxs-lookup"><span data-stu-id="e50f6-112">Capacity</span></span>

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

### <span data-ttu-id="e50f6-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="e50f6-113">-Name</span></span>
<span data-ttu-id="e50f6-114">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e50f6-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e50f6-115">-NodeType</span><span class="sxs-lookup"><span data-stu-id="e50f6-115">-NodeType</span></span>
<span data-ttu-id="e50f6-116">節點類型名稱。</span><span class="sxs-lookup"><span data-stu-id="e50f6-116">The node type name.</span></span>

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

### <span data-ttu-id="e50f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e50f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="e50f6-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e50f6-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e50f6-119">層級</span><span class="sxs-lookup"><span data-stu-id="e50f6-119">-Tier</span></span>
<span data-ttu-id="e50f6-120">Vm Sku 層。</span><span class="sxs-lookup"><span data-stu-id="e50f6-120">Vm Sku Tier.</span></span>

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

### <span data-ttu-id="e50f6-121">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="e50f6-121">-DurabilityLevel</span></span>
<span data-ttu-id="e50f6-122">指定 NodeType 的持久性層級。</span><span class="sxs-lookup"><span data-stu-id="e50f6-122">Specify the durability level of the NodeType.</span></span>

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

### <span data-ttu-id="e50f6-123">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="e50f6-123">-VmPassword</span></span>
<span data-ttu-id="e50f6-124">登入到 Vm 的密碼。</span><span class="sxs-lookup"><span data-stu-id="e50f6-124">The password of login to the Vm.</span></span>

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

### <span data-ttu-id="e50f6-125">-VmSku</span><span class="sxs-lookup"><span data-stu-id="e50f6-125">-VmSku</span></span>
<span data-ttu-id="e50f6-126">Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="e50f6-126">The sku name.</span></span>

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

### <span data-ttu-id="e50f6-127">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="e50f6-127">-VmUserName</span></span>
<span data-ttu-id="e50f6-128">登入到 Vm 的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="e50f6-128">The user name for login to Vm.</span></span>

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

### <span data-ttu-id="e50f6-129">-確認</span><span class="sxs-lookup"><span data-stu-id="e50f6-129">-Confirm</span></span>
<span data-ttu-id="e50f6-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e50f6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e50f6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e50f6-131">-WhatIf</span></span>
<span data-ttu-id="e50f6-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e50f6-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e50f6-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e50f6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e50f6-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e50f6-134">-DefaultProfile</span></span>
<span data-ttu-id="e50f6-135">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e50f6-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e50f6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e50f6-136">CommonParameters</span></span>
<span data-ttu-id="e50f6-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e50f6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e50f6-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e50f6-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e50f6-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e50f6-139">INPUTS</span></span>

### <span data-ttu-id="e50f6-140">System.object</span><span class="sxs-lookup"><span data-stu-id="e50f6-140">System.String</span></span>
<span data-ttu-id="e50f6-141">System.object</span><span class="sxs-lookup"><span data-stu-id="e50f6-141">System.Int32</span></span>

## <span data-ttu-id="e50f6-142">輸出</span><span class="sxs-lookup"><span data-stu-id="e50f6-142">OUTPUTS</span></span>

### <span data-ttu-id="e50f6-143">System.object</span><span class="sxs-lookup"><span data-stu-id="e50f6-143">System.Object</span></span>

## <span data-ttu-id="e50f6-144">筆記</span><span class="sxs-lookup"><span data-stu-id="e50f6-144">NOTES</span></span>

## <span data-ttu-id="e50f6-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="e50f6-145">RELATED LINKS</span></span>

