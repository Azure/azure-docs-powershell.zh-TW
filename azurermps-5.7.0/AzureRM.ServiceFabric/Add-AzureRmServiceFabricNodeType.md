---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 0bae150e60332e4f1bb0ee4f2ee67699c13eb5e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446012"
---
# <span data-ttu-id="b555c-101">Add-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="b555c-101">Add-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="b555c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b555c-102">SYNOPSIS</span></span>
<span data-ttu-id="b555c-103">在現有的群集中新增節點類型。</span><span class="sxs-lookup"><span data-stu-id="b555c-103">Add a new node type to the existing cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b555c-104">句法</span><span class="sxs-lookup"><span data-stu-id="b555c-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -Capacity <Int32>
 -VmUserName <String> -VmPassword <SecureString> [-VmSku <String>] [-Tier <String>]
 [-DurabilityLevel <DurabilityLevel>] -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b555c-105">說明</span><span class="sxs-lookup"><span data-stu-id="b555c-105">DESCRIPTION</span></span>
<span data-ttu-id="b555c-106">在現有的群集中新增節點類型。</span><span class="sxs-lookup"><span data-stu-id="b555c-106">Add a new node type to a existing cluster.</span></span>

## <span data-ttu-id="b555c-107">示例</span><span class="sxs-lookup"><span data-stu-id="b555c-107">EXAMPLES</span></span>

### <span data-ttu-id="b555c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b555c-108">Example 1</span></span>
```
PS c:\> $pwd = ConvertTo-SecureString -String 'Password$123456' -AsPlainText -Force
PS C:\> Add-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'n2' -Capacity 5 -VmUserName 'adminName' -VmPassword $pwd
```

<span data-ttu-id="b555c-109">這個命令會新增一個新的 NodeType "n2" （容量為5），而 vm 管理員名稱是 "adminName"。</span><span class="sxs-lookup"><span data-stu-id="b555c-109">This command will add a new NodeType 'n2' with capacity of 5, and the vm admin name is 'adminName'.</span></span>

## <span data-ttu-id="b555c-110">參數</span><span class="sxs-lookup"><span data-stu-id="b555c-110">PARAMETERS</span></span>

### <span data-ttu-id="b555c-111">-容量</span><span class="sxs-lookup"><span data-stu-id="b555c-111">-Capacity</span></span>
<span data-ttu-id="b555c-112">按需分配</span><span class="sxs-lookup"><span data-stu-id="b555c-112">Capacity</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b555c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b555c-113">-DefaultProfile</span></span>
<span data-ttu-id="b555c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b555c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b555c-115">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="b555c-115">-DurabilityLevel</span></span>
<span data-ttu-id="b555c-116">指定 NodeType 的持久性層級。</span><span class="sxs-lookup"><span data-stu-id="b555c-116">Specify the durability level of the NodeType.</span></span>

```yaml
Type: DurabilityLevel
Parameter Sets: (All)
Aliases: 
Accepted values: Bronze, Silver, Gold

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b555c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b555c-117">-Name</span></span>
<span data-ttu-id="b555c-118">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="b555c-118">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b555c-119">-NodeType</span><span class="sxs-lookup"><span data-stu-id="b555c-119">-NodeType</span></span>
<span data-ttu-id="b555c-120">節點類型名稱。</span><span class="sxs-lookup"><span data-stu-id="b555c-120">The node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b555c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b555c-121">-ResourceGroupName</span></span>
<span data-ttu-id="b555c-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b555c-122">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b555c-123">層級</span><span class="sxs-lookup"><span data-stu-id="b555c-123">-Tier</span></span>
<span data-ttu-id="b555c-124">Vm Sku 層。</span><span class="sxs-lookup"><span data-stu-id="b555c-124">Vm Sku Tier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b555c-125">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="b555c-125">-VmPassword</span></span>
<span data-ttu-id="b555c-126">登入到 Vm 的密碼。</span><span class="sxs-lookup"><span data-stu-id="b555c-126">The password of login to the Vm.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b555c-127">-VmSku</span><span class="sxs-lookup"><span data-stu-id="b555c-127">-VmSku</span></span>
<span data-ttu-id="b555c-128">Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="b555c-128">The sku name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b555c-129">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="b555c-129">-VmUserName</span></span>
<span data-ttu-id="b555c-130">登入到 Vm 的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="b555c-130">The user name for login to Vm.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b555c-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b555c-131">-Confirm</span></span>
<span data-ttu-id="b555c-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b555c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b555c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b555c-133">-WhatIf</span></span>
<span data-ttu-id="b555c-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b555c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b555c-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b555c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b555c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b555c-136">CommonParameters</span></span>
<span data-ttu-id="b555c-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b555c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b555c-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b555c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b555c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b555c-139">INPUTS</span></span>

### <span data-ttu-id="b555c-140">System.object</span><span class="sxs-lookup"><span data-stu-id="b555c-140">System.String</span></span>
<span data-ttu-id="b555c-141">System.object</span><span class="sxs-lookup"><span data-stu-id="b555c-141">System.Int32</span></span>

## <span data-ttu-id="b555c-142">輸出</span><span class="sxs-lookup"><span data-stu-id="b555c-142">OUTPUTS</span></span>

### <span data-ttu-id="b555c-143">System.object</span><span class="sxs-lookup"><span data-stu-id="b555c-143">System.Object</span></span>

## <span data-ttu-id="b555c-144">筆記</span><span class="sxs-lookup"><span data-stu-id="b555c-144">NOTES</span></span>

## <span data-ttu-id="b555c-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b555c-145">RELATED LINKS</span></span>

