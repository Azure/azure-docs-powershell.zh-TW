---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyAssignment.md
ms.openlocfilehash: 97be8f9eef611a87dae045df680d2823dc2f7acb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454111"
---
# <span data-ttu-id="777c3-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="777c3-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="777c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="777c3-102">SYNOPSIS</span></span>
<span data-ttu-id="777c3-103">修改原則分派。</span><span class="sxs-lookup"><span data-stu-id="777c3-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="777c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="777c3-104">SYNTAX</span></span>

### <span data-ttu-id="777c3-105">SetByPolicyAssignmentName (預設) </span><span class="sxs-lookup"><span data-stu-id="777c3-105">SetByPolicyAssignmentName (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="777c3-106">SetByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="777c3-106">SetByPolicyAssignmentId</span></span>
```
Set-AzureRmPolicyAssignment -Id <String> [-DisplayName <String>] [-Description <String>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="777c3-107">說明</span><span class="sxs-lookup"><span data-stu-id="777c3-107">DESCRIPTION</span></span>
<span data-ttu-id="777c3-108">**AzureRmPolicyAssignment** Cmdlet 會修改原則指派。</span><span class="sxs-lookup"><span data-stu-id="777c3-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="777c3-109">依識別碼或名稱和範圍指定作業。</span><span class="sxs-lookup"><span data-stu-id="777c3-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="777c3-110">示例</span><span class="sxs-lookup"><span data-stu-id="777c3-110">EXAMPLES</span></span>

### <span data-ttu-id="777c3-111">範例1：更新顯示名稱</span><span class="sxs-lookup"><span data-stu-id="777c3-111">Example 1: Update the display name</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment" -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName "Do not allow VM creation"
```

<span data-ttu-id="777c3-112">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="777c3-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="777c3-113">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="777c3-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="777c3-114">第二個命令會使用 Get-AzureRmPolicyAssignment Cmdlet 來取得名為 PolicyAssignment 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="777c3-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="777c3-115">該命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="777c3-115">The command stores that object in the $PolicyAssignment variable.</span></span>

<span data-ttu-id="777c3-116">Final 命令會更新由 $PolicyAssignment 的 **ResourceId** 屬性所識別之原則指派的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="777c3-116">The final command updates the display name on the policy assignment identified by the **ResourceId** property of $PolicyAssignment.</span></span>

## <span data-ttu-id="777c3-117">參數</span><span class="sxs-lookup"><span data-stu-id="777c3-117">PARAMETERS</span></span>

### <span data-ttu-id="777c3-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="777c3-118">-ApiVersion</span></span>
<span data-ttu-id="777c3-119">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="777c3-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="777c3-120">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="777c3-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="777c3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="777c3-121">-DefaultProfile</span></span>
<span data-ttu-id="777c3-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="777c3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="777c3-123">-描述</span><span class="sxs-lookup"><span data-stu-id="777c3-123">-Description</span></span>
<span data-ttu-id="777c3-124">原則指派的描述</span><span class="sxs-lookup"><span data-stu-id="777c3-124">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="777c3-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="777c3-125">-DisplayName</span></span>
<span data-ttu-id="777c3-126">指定原則指派的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="777c3-126">Specifies a new display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="777c3-127">-識別碼</span><span class="sxs-lookup"><span data-stu-id="777c3-127">-Id</span></span>
<span data-ttu-id="777c3-128">指定此 Cmdlet 所修改之原則指派的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="777c3-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="777c3-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="777c3-129">-InformationAction</span></span>
<span data-ttu-id="777c3-130">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="777c3-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="777c3-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="777c3-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="777c3-132">持續</span><span class="sxs-lookup"><span data-stu-id="777c3-132">Continue</span></span>
- <span data-ttu-id="777c3-133">理會</span><span class="sxs-lookup"><span data-stu-id="777c3-133">Ignore</span></span>
- <span data-ttu-id="777c3-134">看</span><span class="sxs-lookup"><span data-stu-id="777c3-134">Inquire</span></span>
- <span data-ttu-id="777c3-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="777c3-135">SilentlyContinue</span></span>
- <span data-ttu-id="777c3-136">停止</span><span class="sxs-lookup"><span data-stu-id="777c3-136">Stop</span></span>
- <span data-ttu-id="777c3-137">封存</span><span class="sxs-lookup"><span data-stu-id="777c3-137">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="777c3-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="777c3-138">-InformationVariable</span></span>
<span data-ttu-id="777c3-139">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="777c3-139">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="777c3-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="777c3-140">-Name</span></span>
<span data-ttu-id="777c3-141">指定此 Cmdlet 所修改之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="777c3-141">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="777c3-142">-NotScope</span><span class="sxs-lookup"><span data-stu-id="777c3-142">-NotScope</span></span>
<span data-ttu-id="777c3-143">原則指派不是作用中的範圍。</span><span class="sxs-lookup"><span data-stu-id="777c3-143">The policy assignment not scopes.</span></span>

```yaml
Type: String[]
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="777c3-144">-預先</span><span class="sxs-lookup"><span data-stu-id="777c3-144">-Pre</span></span>
<span data-ttu-id="777c3-145">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="777c3-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="777c3-146">-範圍</span><span class="sxs-lookup"><span data-stu-id="777c3-146">-Scope</span></span>
<span data-ttu-id="777c3-147">指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="777c3-147">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="777c3-148">-Sku</span><span class="sxs-lookup"><span data-stu-id="777c3-148">-Sku</span></span>
<span data-ttu-id="777c3-149">代表 sku 屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="777c3-149">A hash table which represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="777c3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="777c3-150">CommonParameters</span></span>
<span data-ttu-id="777c3-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="777c3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="777c3-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="777c3-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="777c3-153">輸入</span><span class="sxs-lookup"><span data-stu-id="777c3-153">INPUTS</span></span>

### <span data-ttu-id="777c3-154">所有</span><span class="sxs-lookup"><span data-stu-id="777c3-154">None</span></span>
<span data-ttu-id="777c3-155">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="777c3-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="777c3-156">輸出</span><span class="sxs-lookup"><span data-stu-id="777c3-156">OUTPUTS</span></span>

### <span data-ttu-id="777c3-157">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="777c3-157">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="777c3-158">筆記</span><span class="sxs-lookup"><span data-stu-id="777c3-158">NOTES</span></span>

## <span data-ttu-id="777c3-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="777c3-159">RELATED LINKS</span></span>

[<span data-ttu-id="777c3-160">AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="777c3-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="777c3-161">新-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="777c3-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="777c3-162">移除-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="777c3-162">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


