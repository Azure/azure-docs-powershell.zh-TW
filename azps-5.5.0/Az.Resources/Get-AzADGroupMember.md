---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 984b5ef9a1ff19142ef044e1f3c919f8fb2a3dce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128466"
---
# <span data-ttu-id="db21d-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="db21d-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="db21d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db21d-102">SYNOPSIS</span></span>
<span data-ttu-id="db21d-103">列出目前租使用者中 AD 群組的成員。</span><span class="sxs-lookup"><span data-stu-id="db21d-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="db21d-104">句法</span><span class="sxs-lookup"><span data-stu-id="db21d-104">SYNTAX</span></span>

### <span data-ttu-id="db21d-105">ObjectIdParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="db21d-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="db21d-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db21d-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="db21d-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db21d-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="db21d-108">說明</span><span class="sxs-lookup"><span data-stu-id="db21d-108">DESCRIPTION</span></span>
<span data-ttu-id="db21d-109">列出目前租使用者中 AD 群組的成員。</span><span class="sxs-lookup"><span data-stu-id="db21d-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="db21d-110">示例</span><span class="sxs-lookup"><span data-stu-id="db21d-110">EXAMPLES</span></span>

### <span data-ttu-id="db21d-111">範例1：依 AD 群組物件識別碼列出成員</span><span class="sxs-lookup"><span data-stu-id="db21d-111">Example 1: List members by AD group object id</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="db21d-112">使用物件 id ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE」列出 AD 群組的成員。</span><span class="sxs-lookup"><span data-stu-id="db21d-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="db21d-113">範例2：使用分頁依據 AD 群組物件識別碼列出成員</span><span class="sxs-lookup"><span data-stu-id="db21d-113">Example 2: List members by AD group object id using paging</span></span>

```powershell
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="db21d-114">列出 AD 群組中的第一個100成員，其物件 id 為 ' 85F89C90-780E-4AA6-9F4F-6F268D322EEE」。</span><span class="sxs-lookup"><span data-stu-id="db21d-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="db21d-115">範例3：依管道列出成員</span><span class="sxs-lookup"><span data-stu-id="db21d-115">Example 3: List members by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="db21d-116">取得物件 id 為 "85F89C90-780E-4AA6-9F4F-6F268D322EEE" 的 AD 群組，並將其管道至 Get-AzADGroupMember Cmdlet，以列出該群組中的所有成員。</span><span class="sxs-lookup"><span data-stu-id="db21d-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="db21d-117">參數</span><span class="sxs-lookup"><span data-stu-id="db21d-117">PARAMETERS</span></span>

### <span data-ttu-id="db21d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db21d-118">-DefaultProfile</span></span>
<span data-ttu-id="db21d-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="db21d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db21d-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="db21d-120">-GroupDisplayName</span></span>
<span data-ttu-id="db21d-121">群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="db21d-121">The display name of the group.</span></span>

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

### <span data-ttu-id="db21d-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="db21d-122">-GroupObject</span></span>
<span data-ttu-id="db21d-123">您正在列舉其成員的群組物件。</span><span class="sxs-lookup"><span data-stu-id="db21d-123">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db21d-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="db21d-124">-GroupObjectId</span></span>
<span data-ttu-id="db21d-125">群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="db21d-125">Object Id of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db21d-126">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="db21d-126">-IncludeTotalCount</span></span>
<span data-ttu-id="db21d-127">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="db21d-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="db21d-128">這個參數目前不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="db21d-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="db21d-129">-略過</span><span class="sxs-lookup"><span data-stu-id="db21d-129">-Skip</span></span>
<span data-ttu-id="db21d-130">忽略前 N 個物件，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="db21d-130">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="db21d-131">-優先</span><span class="sxs-lookup"><span data-stu-id="db21d-131">-First</span></span>
<span data-ttu-id="db21d-132">要傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="db21d-132">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="db21d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db21d-133">CommonParameters</span></span>
<span data-ttu-id="db21d-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db21d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db21d-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="db21d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db21d-136">輸入</span><span class="sxs-lookup"><span data-stu-id="db21d-136">INPUTS</span></span>

### <span data-ttu-id="db21d-137">System.object</span><span class="sxs-lookup"><span data-stu-id="db21d-137">System.String</span></span>

### <span data-ttu-id="db21d-138">PSADGroup （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="db21d-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="db21d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="db21d-139">OUTPUTS</span></span>

### <span data-ttu-id="db21d-140">PSADObject （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="db21d-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="db21d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="db21d-141">NOTES</span></span>

## <span data-ttu-id="db21d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="db21d-142">RELATED LINKS</span></span>

[<span data-ttu-id="db21d-143">AzADUser</span><span class="sxs-lookup"><span data-stu-id="db21d-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="db21d-144">AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="db21d-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

