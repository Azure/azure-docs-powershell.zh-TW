---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: ffc04a6b1560845a0c29db4d000270fe91aa8ff4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457380"
---
# <span data-ttu-id="e0f29-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="e0f29-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="e0f29-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0f29-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f29-103">列出目前租使用者中 AD 群組的成員。</span><span class="sxs-lookup"><span data-stu-id="e0f29-103">Lists members of an AD group in the current tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0f29-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0f29-104">SYNTAX</span></span>

### <span data-ttu-id="e0f29-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e0f29-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e0f29-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0f29-106">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e0f29-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0f29-107">GroupObjectParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="e0f29-108">說明</span><span class="sxs-lookup"><span data-stu-id="e0f29-108">DESCRIPTION</span></span>
<span data-ttu-id="e0f29-109">列出目前租使用者中 AD 群組的成員。</span><span class="sxs-lookup"><span data-stu-id="e0f29-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="e0f29-110">示例</span><span class="sxs-lookup"><span data-stu-id="e0f29-110">EXAMPLES</span></span>

### <span data-ttu-id="e0f29-111">範例 1-依 AD 群組物件識別碼列出成員</span><span class="sxs-lookup"><span data-stu-id="e0f29-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="e0f29-112">使用物件 id ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE」列出 AD 群組的成員。</span><span class="sxs-lookup"><span data-stu-id="e0f29-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="e0f29-113">範例 2-使用分頁的 AD 群組物件識別碼來列出成員</span><span class="sxs-lookup"><span data-stu-id="e0f29-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="e0f29-114">列出 AD 群組中的第一個100成員，其物件 id 為 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE」。</span><span class="sxs-lookup"><span data-stu-id="e0f29-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="e0f29-115">範例 3-依管道列出成員</span><span class="sxs-lookup"><span data-stu-id="e0f29-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzureRmADGroupMember
```

<span data-ttu-id="e0f29-116">取得物件 id 為 "85F89C90-780E-4AA6-9F4F-6F268D322EEE" 的 AD 群組，並將其管道至 Get-AzureRmADGroupMember Cmdlet，以列出該群組中的所有成員。</span><span class="sxs-lookup"><span data-stu-id="e0f29-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzureRmADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="e0f29-117">參數</span><span class="sxs-lookup"><span data-stu-id="e0f29-117">PARAMETERS</span></span>

### <span data-ttu-id="e0f29-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f29-118">-DefaultProfile</span></span>
<span data-ttu-id="e0f29-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e0f29-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0f29-120">-優先</span><span class="sxs-lookup"><span data-stu-id="e0f29-120">-First</span></span>
<span data-ttu-id="e0f29-121">要傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="e0f29-121">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f29-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="e0f29-122">-GroupDisplayName</span></span>
<span data-ttu-id="e0f29-123">群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="e0f29-123">The display name of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f29-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="e0f29-124">-GroupObject</span></span>
<span data-ttu-id="e0f29-125">您正在列舉其成員的群組物件。</span><span class="sxs-lookup"><span data-stu-id="e0f29-125">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f29-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="e0f29-126">-GroupObjectId</span></span>
<span data-ttu-id="e0f29-127">群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0f29-127">Object Id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0f29-128">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="e0f29-128">-IncludeTotalCount</span></span>
<span data-ttu-id="e0f29-129">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="e0f29-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="e0f29-130">這個參數目前不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="e0f29-130">Currently, this parameter does nothing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f29-131">-略過</span><span class="sxs-lookup"><span data-stu-id="e0f29-131">-Skip</span></span>
<span data-ttu-id="e0f29-132">忽略前 N 個物件，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="e0f29-132">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0f29-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f29-133">CommonParameters</span></span>
<span data-ttu-id="e0f29-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0f29-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f29-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0f29-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f29-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e0f29-136">INPUTS</span></span>

### <span data-ttu-id="e0f29-137">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="e0f29-137">System.Guid</span></span>

### <span data-ttu-id="e0f29-138">Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup</span><span class="sxs-lookup"><span data-stu-id="e0f29-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="e0f29-139">參數： GroupObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="e0f29-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="e0f29-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e0f29-140">OUTPUTS</span></span>

### <span data-ttu-id="e0f29-141">Microsoft.Azure.Graph.RBAC.Version1_6 PSADObject</span><span class="sxs-lookup"><span data-stu-id="e0f29-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="e0f29-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e0f29-142">NOTES</span></span>

## <span data-ttu-id="e0f29-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0f29-143">RELATED LINKS</span></span>

[<span data-ttu-id="e0f29-144">AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="e0f29-144">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="e0f29-145">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e0f29-145">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

