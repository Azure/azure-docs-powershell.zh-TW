---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 764b2d091b0019cc4231828066b4067c5f054476
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279084"
---
# <span data-ttu-id="76feb-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="76feb-101">Get-AzADGroup</span></span>

## <span data-ttu-id="76feb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76feb-102">SYNOPSIS</span></span>
<span data-ttu-id="76feb-103">篩選 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="76feb-103">Filters active directory groups.</span></span>

## <span data-ttu-id="76feb-104">句法</span><span class="sxs-lookup"><span data-stu-id="76feb-104">SYNTAX</span></span>

### <span data-ttu-id="76feb-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="76feb-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="76feb-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="76feb-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="76feb-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="76feb-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="76feb-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76feb-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="76feb-109">說明</span><span class="sxs-lookup"><span data-stu-id="76feb-109">DESCRIPTION</span></span>
<span data-ttu-id="76feb-110">篩選 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="76feb-110">Filters active directory groups.</span></span>

## <span data-ttu-id="76feb-111">示例</span><span class="sxs-lookup"><span data-stu-id="76feb-111">EXAMPLES</span></span>

### <span data-ttu-id="76feb-112">範例1：列出所有廣告群組</span><span class="sxs-lookup"><span data-stu-id="76feb-112">Example 1: List all AD groups</span></span>
```powershell
PS C:\> Get-AzADGroup
```

<span data-ttu-id="76feb-113">列出租使用者中的所有廣告群組。</span><span class="sxs-lookup"><span data-stu-id="76feb-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="76feb-114">範例2：使用分頁列出所有 AD 群組</span><span class="sxs-lookup"><span data-stu-id="76feb-114">Example 2: List all AD groups using paging</span></span>

```powershell
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="76feb-115">列出租使用者中的第一個 100 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="76feb-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="76feb-116">範例3：透過物件識別碼取得 AD 群組</span><span class="sxs-lookup"><span data-stu-id="76feb-116">Example 3: Get AD group by object id</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="76feb-117">取得物件 id 為 "85F89C90-780E-4AA6-9F4F-6F268D322EEE" 的 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="76feb-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="76feb-118">範例4：依搜尋字串列出群組</span><span class="sxs-lookup"><span data-stu-id="76feb-118">Example 4: List groups by search string</span></span>

```powershell
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="76feb-119">列出顯示名稱以「Joe」開頭的所有廣告群組。</span><span class="sxs-lookup"><span data-stu-id="76feb-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="76feb-120">參數</span><span class="sxs-lookup"><span data-stu-id="76feb-120">PARAMETERS</span></span>

### <span data-ttu-id="76feb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76feb-121">-DefaultProfile</span></span>
<span data-ttu-id="76feb-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="76feb-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76feb-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="76feb-123">-DisplayName</span></span>
<span data-ttu-id="76feb-124">群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="76feb-124">The display name of the group.</span></span>

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

### <span data-ttu-id="76feb-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="76feb-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="76feb-126">用來尋找以所提供字串開頭的群組。</span><span class="sxs-lookup"><span data-stu-id="76feb-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="76feb-127">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="76feb-127">-ObjectId</span></span>
<span data-ttu-id="76feb-128">群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="76feb-128">Object id of the group.</span></span>

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

### <span data-ttu-id="76feb-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="76feb-129">-IncludeTotalCount</span></span>
<span data-ttu-id="76feb-130">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="76feb-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="76feb-131">這個參數目前不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="76feb-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="76feb-132">-略過</span><span class="sxs-lookup"><span data-stu-id="76feb-132">-Skip</span></span>
<span data-ttu-id="76feb-133">忽略前 N 個物件，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="76feb-133">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="76feb-134">-優先</span><span class="sxs-lookup"><span data-stu-id="76feb-134">-First</span></span>
<span data-ttu-id="76feb-135">要傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="76feb-135">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="76feb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76feb-136">CommonParameters</span></span>
<span data-ttu-id="76feb-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76feb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76feb-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="76feb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76feb-139">輸入</span><span class="sxs-lookup"><span data-stu-id="76feb-139">INPUTS</span></span>

### <span data-ttu-id="76feb-140">System.object</span><span class="sxs-lookup"><span data-stu-id="76feb-140">System.String</span></span>

### <span data-ttu-id="76feb-141">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="76feb-141">System.Guid</span></span>

## <span data-ttu-id="76feb-142">輸出</span><span class="sxs-lookup"><span data-stu-id="76feb-142">OUTPUTS</span></span>

### <span data-ttu-id="76feb-143">PSADGroup （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="76feb-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="76feb-144">筆記</span><span class="sxs-lookup"><span data-stu-id="76feb-144">NOTES</span></span>

## <span data-ttu-id="76feb-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="76feb-145">RELATED LINKS</span></span>

[<span data-ttu-id="76feb-146">AzADUser</span><span class="sxs-lookup"><span data-stu-id="76feb-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="76feb-147">AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="76feb-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="76feb-148">AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="76feb-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

