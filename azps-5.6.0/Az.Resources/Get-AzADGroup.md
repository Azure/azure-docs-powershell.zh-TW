---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 84e2942037ba0d01425ca85530d33a042544dafc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912330"
---
# <span data-ttu-id="9e630-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="9e630-101">Get-AzADGroup</span></span>

## <span data-ttu-id="9e630-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9e630-102">SYNOPSIS</span></span>
<span data-ttu-id="9e630-103">篩選 Active Directory 群組。</span><span class="sxs-lookup"><span data-stu-id="9e630-103">Filters active directory groups.</span></span>

## <span data-ttu-id="9e630-104">語法</span><span class="sxs-lookup"><span data-stu-id="9e630-104">SYNTAX</span></span>

### <span data-ttu-id="9e630-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9e630-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9e630-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e630-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9e630-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e630-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="9e630-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e630-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="9e630-109">描述</span><span class="sxs-lookup"><span data-stu-id="9e630-109">DESCRIPTION</span></span>
<span data-ttu-id="9e630-110">篩選 Active Directory 群組。</span><span class="sxs-lookup"><span data-stu-id="9e630-110">Filters active directory groups.</span></span>

## <span data-ttu-id="9e630-111">例子</span><span class="sxs-lookup"><span data-stu-id="9e630-111">EXAMPLES</span></span>

### <span data-ttu-id="9e630-112">範例 1：列出所有 AD 群組</span><span class="sxs-lookup"><span data-stu-id="9e630-112">Example 1: List all AD groups</span></span>
```powershell
PS C:\> Get-AzADGroup
```

<span data-ttu-id="9e630-113">列出租使用者中所有的 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="9e630-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="9e630-114">範例 2：使用分頁功能列出所有 AD 群組</span><span class="sxs-lookup"><span data-stu-id="9e630-114">Example 2: List all AD groups using paging</span></span>

```powershell
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="9e630-115">列出租使用者中前 100 個 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="9e630-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="9e630-116">範例 3：根據物件識別碼取得 AD 群組</span><span class="sxs-lookup"><span data-stu-id="9e630-116">Example 3: Get AD group by object id</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="9e630-117">使用物件識別碼為 '85F89C90-780E-4AA6-9F4F-6F268D322EEE'的 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="9e630-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="9e630-118">範例 4：按搜尋字串列出群組</span><span class="sxs-lookup"><span data-stu-id="9e630-118">Example 4: List groups by search string</span></span>

```powershell
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="9e630-119">列出顯示名稱以 "Joe" 開頭的所有 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="9e630-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="9e630-120">參數</span><span class="sxs-lookup"><span data-stu-id="9e630-120">PARAMETERS</span></span>

### <span data-ttu-id="9e630-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e630-121">-DefaultProfile</span></span>
<span data-ttu-id="9e630-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="9e630-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e630-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9e630-123">-DisplayName</span></span>
<span data-ttu-id="9e630-124">群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="9e630-124">The display name of the group.</span></span>

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

### <span data-ttu-id="9e630-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="9e630-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="9e630-126">用來尋找以所提供的字串開頭的群組。</span><span class="sxs-lookup"><span data-stu-id="9e630-126">Used to find groups that begin with the provided string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e630-127">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9e630-127">-ObjectId</span></span>
<span data-ttu-id="9e630-128">群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="9e630-128">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e630-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="9e630-129">-IncludeTotalCount</span></span>
<span data-ttu-id="9e630-130">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="9e630-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="9e630-131">目前，此參數沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="9e630-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="9e630-132">-略過</span><span class="sxs-lookup"><span data-stu-id="9e630-132">-Skip</span></span>
<span data-ttu-id="9e630-133">忽略前 N 個物件，然後獲得其餘的物件。</span><span class="sxs-lookup"><span data-stu-id="9e630-133">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="9e630-134">-第一個</span><span class="sxs-lookup"><span data-stu-id="9e630-134">-First</span></span>
<span data-ttu-id="9e630-135">要返回的物件數量上限。</span><span class="sxs-lookup"><span data-stu-id="9e630-135">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="9e630-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e630-136">CommonParameters</span></span>
<span data-ttu-id="9e630-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9e630-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e630-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e630-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e630-139">輸入</span><span class="sxs-lookup"><span data-stu-id="9e630-139">INPUTS</span></span>

### <span data-ttu-id="9e630-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9e630-140">System.String</span></span>

### <span data-ttu-id="9e630-141">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9e630-141">System.Guid</span></span>

## <span data-ttu-id="9e630-142">輸出</span><span class="sxs-lookup"><span data-stu-id="9e630-142">OUTPUTS</span></span>

### <span data-ttu-id="9e630-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="9e630-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="9e630-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9e630-144">NOTES</span></span>

## <span data-ttu-id="9e630-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e630-145">RELATED LINKS</span></span>

[<span data-ttu-id="9e630-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="9e630-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="9e630-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9e630-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="9e630-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="9e630-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

