---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 0604c7bd8f4f016f908eb7e9c93ff6b9d95db979
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624998"
---
# <span data-ttu-id="436a4-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="436a4-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="436a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="436a4-102">SYNOPSIS</span></span>
<span data-ttu-id="436a4-103">取得原則指派。</span><span class="sxs-lookup"><span data-stu-id="436a4-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="436a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="436a4-104">SYNTAX</span></span>

### <span data-ttu-id="436a4-105">GetAllPolicyAssignments (預設) </span><span class="sxs-lookup"><span data-stu-id="436a4-105">GetAllPolicyAssignments (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="436a4-106">GetPolicyAssignmentName</span><span class="sxs-lookup"><span data-stu-id="436a4-106">GetPolicyAssignmentName</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="436a4-107">GetPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="436a4-107">GetPolicyAssignmentId</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="436a4-108">說明</span><span class="sxs-lookup"><span data-stu-id="436a4-108">DESCRIPTION</span></span>
<span data-ttu-id="436a4-109">**AzureRmPolicyAssignment** Cmdlet 會取得所有原則指派或特定作業。</span><span class="sxs-lookup"><span data-stu-id="436a4-109">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="436a4-110">找出要依名稱、範圍或識別碼來取得的原則指派。</span><span class="sxs-lookup"><span data-stu-id="436a4-110">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="436a4-111">示例</span><span class="sxs-lookup"><span data-stu-id="436a4-111">EXAMPLES</span></span>

### <span data-ttu-id="436a4-112">範例1：取得所有原則指派</span><span class="sxs-lookup"><span data-stu-id="436a4-112">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="436a4-113">這個命令會取得所有原則指派。</span><span class="sxs-lookup"><span data-stu-id="436a4-113">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="436a4-114">範例2：取得特定原則指派</span><span class="sxs-lookup"><span data-stu-id="436a4-114">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="436a4-115">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="436a4-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="436a4-116">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="436a4-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="436a4-117">第二個命令會針對 $ResourceGroup 的 **ResourceId** 屬性所識別的範圍，取得名為 PolicyAssignment07 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="436a4-117">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="436a4-118">參數</span><span class="sxs-lookup"><span data-stu-id="436a4-118">PARAMETERS</span></span>

### <span data-ttu-id="436a4-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="436a4-119">-ApiVersion</span></span>
<span data-ttu-id="436a4-120">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="436a4-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="436a4-121">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="436a4-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="436a4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="436a4-122">-DefaultProfile</span></span>
<span data-ttu-id="436a4-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="436a4-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="436a4-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="436a4-124">-Id</span></span>
<span data-ttu-id="436a4-125">指定此 Cmdlet 所取得之原則指派的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="436a4-125">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="436a4-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="436a4-126">-InformationAction</span></span>
<span data-ttu-id="436a4-127">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="436a4-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="436a4-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="436a4-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="436a4-129">持續</span><span class="sxs-lookup"><span data-stu-id="436a4-129">Continue</span></span>
- <span data-ttu-id="436a4-130">理會</span><span class="sxs-lookup"><span data-stu-id="436a4-130">Ignore</span></span>
- <span data-ttu-id="436a4-131">看</span><span class="sxs-lookup"><span data-stu-id="436a4-131">Inquire</span></span>
- <span data-ttu-id="436a4-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="436a4-132">SilentlyContinue</span></span>
- <span data-ttu-id="436a4-133">停止</span><span class="sxs-lookup"><span data-stu-id="436a4-133">Stop</span></span>
- <span data-ttu-id="436a4-134">封存</span><span class="sxs-lookup"><span data-stu-id="436a4-134">Suspend</span></span>

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

### <span data-ttu-id="436a4-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="436a4-135">-InformationVariable</span></span>
<span data-ttu-id="436a4-136">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="436a4-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="436a4-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="436a4-137">-Name</span></span>
<span data-ttu-id="436a4-138">指定此 Cmdlet 所取得之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="436a4-138">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="436a4-139">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="436a4-139">-PolicyDefinitionId</span></span>
<span data-ttu-id="436a4-140">指定此 Cmdlet 所取得之原則指派的原則定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="436a4-140">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName, GetPolicyAssignmentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="436a4-141">-預先</span><span class="sxs-lookup"><span data-stu-id="436a4-141">-Pre</span></span>
<span data-ttu-id="436a4-142">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="436a4-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="436a4-143">-範圍</span><span class="sxs-lookup"><span data-stu-id="436a4-143">-Scope</span></span>
<span data-ttu-id="436a4-144">針對此 Cmdlet 所取得的作業，指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="436a4-144">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: GetPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="436a4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="436a4-145">CommonParameters</span></span>
<span data-ttu-id="436a4-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="436a4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="436a4-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="436a4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="436a4-148">輸入</span><span class="sxs-lookup"><span data-stu-id="436a4-148">INPUTS</span></span>

### <span data-ttu-id="436a4-149">所有</span><span class="sxs-lookup"><span data-stu-id="436a4-149">None</span></span>
<span data-ttu-id="436a4-150">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="436a4-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="436a4-151">輸出</span><span class="sxs-lookup"><span data-stu-id="436a4-151">OUTPUTS</span></span>

### <span data-ttu-id="436a4-152">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="436a4-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="436a4-153">筆記</span><span class="sxs-lookup"><span data-stu-id="436a4-153">NOTES</span></span>

## <span data-ttu-id="436a4-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="436a4-154">RELATED LINKS</span></span>

[<span data-ttu-id="436a4-155">新-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="436a4-155">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="436a4-156">移除-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="436a4-156">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="436a4-157">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="436a4-157">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


