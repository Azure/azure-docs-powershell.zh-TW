---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResource.md
ms.openlocfilehash: 2161c3c4bc81721c0d99b88ab0adfc43beac8eee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448569"
---
# <span data-ttu-id="ecb75-101">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ecb75-101">Get-AzureRmResource</span></span>

## <span data-ttu-id="ecb75-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ecb75-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb75-103">取得資源。</span><span class="sxs-lookup"><span data-stu-id="ecb75-103">Gets resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecb75-104">句法</span><span class="sxs-lookup"><span data-stu-id="ecb75-104">SYNTAX</span></span>

### <span data-ttu-id="ecb75-105">GetAllResources (預設) </span><span class="sxs-lookup"><span data-stu-id="ecb75-105">GetAllResources (Default)</span></span>
```
Get-AzureRmResource [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb75-106">GetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ecb75-106">GetByResourceId</span></span>
```
Get-AzureRmResource -ResourceId <String> [-ExpandProperties] [-ODataQuery <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb75-107">GetByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="ecb75-107">GetByTenantLevel</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb75-108">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="ecb75-108">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-Top <Int32>] [-ODataQuery <String>]
 [-TenantLevel] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb75-109">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="ecb75-109">GetByNameAndGroup</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ecb75-110">GetByResourceNameAndType</span><span class="sxs-lookup"><span data-stu-id="ecb75-110">GetByResourceNameAndType</span></span>
```
Get-AzureRmResource [-ResourceName <String>] [-ResourceType <String>] [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-IsCollection] [-ODataQuery <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb75-111">GetByNameGroupAndType</span><span class="sxs-lookup"><span data-stu-id="ecb75-111">GetByNameGroupAndType</span></span>
```
Get-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ExpandProperties] [-ODataQuery <String>] -ResourceGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecb75-112">GetResourceCollection</span><span class="sxs-lookup"><span data-stu-id="ecb75-112">GetResourceCollection</span></span>
```
Get-AzureRmResource [-ResourceType <String>] [-ExtensionResourceType <String>] [-ExpandProperties]
 [-IsCollection] [-ODataQuery <String>] [-ResourceGroupName <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecb75-113">說明</span><span class="sxs-lookup"><span data-stu-id="ecb75-113">DESCRIPTION</span></span>
<span data-ttu-id="ecb75-114">**AzureRmResource** Cmdlet 會取得 Azure 資源。</span><span class="sxs-lookup"><span data-stu-id="ecb75-114">The **Get-AzureRmResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="ecb75-115">示例</span><span class="sxs-lookup"><span data-stu-id="ecb75-115">EXAMPLES</span></span>

### <span data-ttu-id="ecb75-116">範例1：取得特定類型的所有資源</span><span class="sxs-lookup"><span data-stu-id="ecb75-116">Example 1: Get all the resources of a particular type</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType microsoft.web/sites
```

<span data-ttu-id="ecb75-117">這個命令會在 ResourceGroup11 下取得類型為 [microsoft. 網站] 的資源。</span><span class="sxs-lookup"><span data-stu-id="ecb75-117">This command gets a resource of the type microsoft.web/sites under ResourceGroup11.</span></span>

### <span data-ttu-id="ecb75-118">範例2：依名稱取得資源</span><span class="sxs-lookup"><span data-stu-id="ecb75-118">Example 2: Get a resource by name</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceName ContosoWebsite
```

<span data-ttu-id="ecb75-119">這個命令會在 [ResourceGroup11] 下取得名為 ContosoWebsite 的資源。</span><span class="sxs-lookup"><span data-stu-id="ecb75-119">This command gets a resource  named ContosoWebsite under ResourceGroup11.</span></span>

### <span data-ttu-id="ecb75-120">範例3：在資源群組中顯示儲存空間帳戶的所有狀態</span><span class="sxs-lookup"><span data-stu-id="ecb75-120">Example 3: Show all the status of storage accounts in a Resource Group</span></span>
```
PS C:\>Get-AzureRmResource -ResourceGroupName ResourceGroup11 -ResourceType Microsoft.ClassicStorage/storageAccounts -ExpandProperties |
   Select * -Expand Properties |
   Sort Name |
   Format-Table Name,Status*
```

## <span data-ttu-id="ecb75-121">參數</span><span class="sxs-lookup"><span data-stu-id="ecb75-121">PARAMETERS</span></span>

### <span data-ttu-id="ecb75-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ecb75-122">-ApiVersion</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb75-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb75-123">-DefaultProfile</span></span>
<span data-ttu-id="ecb75-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ecb75-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ecb75-125">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="ecb75-125">-ExpandProperties</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb75-126">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="ecb75-126">-ExtensionResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb75-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="ecb75-127">-ExtensionResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetByNameGroupAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb75-128">-IsCollection</span><span class="sxs-lookup"><span data-stu-id="ecb75-128">-IsCollection</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType, GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb75-129">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ecb75-129">-ODataQuery</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb75-130">-預先</span><span class="sxs-lookup"><span data-stu-id="ecb75-130">-Pre</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb75-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecb75-131">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb75-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecb75-132">-ResourceId</span></span>
<span data-ttu-id="ecb75-133">指定完全限定的資源識別碼，包括訂閱，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="ecb75-133">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span> 

<span data-ttu-id="ecb75-134">`/subscriptions/`訂閱識別碼`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="ecb75-134">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

<span data-ttu-id="ecb75-135">這個 Cmdlet 會取得具有此識別碼的資源。</span><span class="sxs-lookup"><span data-stu-id="ecb75-135">This cmdlet gets the resource that has this ID.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb75-136">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="ecb75-136">-ResourceName</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByNameAndGroup, GetByResourceNameAndType
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb75-137">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ecb75-137">-ResourceType</span></span>
```yaml
Type: String
Parameter Sets: GetByTenantLevel, GetByNameGroupAndType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByResourceNameAndType
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetResourceCollection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb75-138">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="ecb75-138">-TenantLevel</span></span>
<span data-ttu-id="ecb75-139">表示此 Cmdlet 在租使用者層級運作。</span><span class="sxs-lookup"><span data-stu-id="ecb75-139">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetByTenantLevel, GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb75-140">-上方</span><span class="sxs-lookup"><span data-stu-id="ecb75-140">-Top</span></span>
```yaml
Type: Int32
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecb75-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb75-141">CommonParameters</span></span>
<span data-ttu-id="ecb75-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ecb75-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb75-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ecb75-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb75-144">輸入</span><span class="sxs-lookup"><span data-stu-id="ecb75-144">INPUTS</span></span>

### <span data-ttu-id="ecb75-145">所有</span><span class="sxs-lookup"><span data-stu-id="ecb75-145">None</span></span>
<span data-ttu-id="ecb75-146">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ecb75-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ecb75-147">輸出</span><span class="sxs-lookup"><span data-stu-id="ecb75-147">OUTPUTS</span></span>

### <span data-ttu-id="ecb75-148">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="ecb75-148">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="ecb75-149">筆記</span><span class="sxs-lookup"><span data-stu-id="ecb75-149">NOTES</span></span>

## <span data-ttu-id="ecb75-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="ecb75-150">RELATED LINKS</span></span>

[<span data-ttu-id="ecb75-151">尋找-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ecb75-151">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="ecb75-152">移動流覽 AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ecb75-152">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="ecb75-153">新-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ecb75-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="ecb75-154">移除-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ecb75-154">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="ecb75-155">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="ecb75-155">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


