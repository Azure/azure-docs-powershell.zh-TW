---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 11a28cb8848c197d9d766b05833e8c0ca3106412
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448001"
---
# <span data-ttu-id="12759-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="12759-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="12759-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12759-102">SYNOPSIS</span></span>
<span data-ttu-id="12759-103">取得原則指派。</span><span class="sxs-lookup"><span data-stu-id="12759-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12759-104">句法</span><span class="sxs-lookup"><span data-stu-id="12759-104">SYNTAX</span></span>

### <span data-ttu-id="12759-105">清單所有原則指派參數設定。</span><span class="sxs-lookup"><span data-stu-id="12759-105">The list all policy assignments parameter set.</span></span> <span data-ttu-id="12759-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="12759-106">(Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="12759-107">原則指派名稱參數已設定。</span><span class="sxs-lookup"><span data-stu-id="12759-107">The policy assignment name parameter set.</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] -Scope <String> [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="12759-108">原則指派識別碼參數已設定。</span><span class="sxs-lookup"><span data-stu-id="12759-108">The policy assignment Id parameter set.</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="12759-109">說明</span><span class="sxs-lookup"><span data-stu-id="12759-109">DESCRIPTION</span></span>
<span data-ttu-id="12759-110">**AzureRmPolicyAssignment** Cmdlet 會取得所有原則指派或特定作業。</span><span class="sxs-lookup"><span data-stu-id="12759-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="12759-111">找出要依名稱、範圍或識別碼來取得的原則指派。</span><span class="sxs-lookup"><span data-stu-id="12759-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="12759-112">示例</span><span class="sxs-lookup"><span data-stu-id="12759-112">EXAMPLES</span></span>

### <span data-ttu-id="12759-113">範例1：取得所有原則指派</span><span class="sxs-lookup"><span data-stu-id="12759-113">Example 1: Get all policy assignments</span></span>
```
PS C:\>Get-AzureRmPolicyAssignment
```

<span data-ttu-id="12759-114">這個命令會取得所有原則指派。</span><span class="sxs-lookup"><span data-stu-id="12759-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="12759-115">範例2：取得特定原則指派</span><span class="sxs-lookup"><span data-stu-id="12759-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="12759-116">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="12759-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="12759-117">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="12759-117">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="12759-118">第二個命令會針對 $ResourceGroup 的 **ResourceId** 屬性所識別的範圍，取得名為 PolicyAssignment07 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="12759-118">The second command get the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

## <span data-ttu-id="12759-119">參數</span><span class="sxs-lookup"><span data-stu-id="12759-119">PARAMETERS</span></span>

### <span data-ttu-id="12759-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="12759-120">-ApiVersion</span></span>
<span data-ttu-id="12759-121">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="12759-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="12759-122">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="12759-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12759-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="12759-123">-Id</span></span>
<span data-ttu-id="12759-124">指定此 Cmdlet 所取得之原則指派的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="12759-124">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12759-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="12759-125">-InformationAction</span></span>
<span data-ttu-id="12759-126">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="12759-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="12759-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="12759-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="12759-128">持續</span><span class="sxs-lookup"><span data-stu-id="12759-128">Continue</span></span>
- <span data-ttu-id="12759-129">理會</span><span class="sxs-lookup"><span data-stu-id="12759-129">Ignore</span></span>
- <span data-ttu-id="12759-130">看</span><span class="sxs-lookup"><span data-stu-id="12759-130">Inquire</span></span>
- <span data-ttu-id="12759-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="12759-131">SilentlyContinue</span></span>
- <span data-ttu-id="12759-132">停止</span><span class="sxs-lookup"><span data-stu-id="12759-132">Stop</span></span>
- <span data-ttu-id="12759-133">封存</span><span class="sxs-lookup"><span data-stu-id="12759-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12759-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="12759-134">-InformationVariable</span></span>
<span data-ttu-id="12759-135">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="12759-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12759-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="12759-136">-Name</span></span>
<span data-ttu-id="12759-137">指定此 Cmdlet 所取得之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="12759-137">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12759-138">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="12759-138">-PolicyDefinitionId</span></span>
<span data-ttu-id="12759-139">指定此 Cmdlet 所取得之原則指派的原則定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="12759-139">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set., The policy assignment Id parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12759-140">-預先</span><span class="sxs-lookup"><span data-stu-id="12759-140">-Pre</span></span>
<span data-ttu-id="12759-141">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="12759-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="12759-142">-範圍</span><span class="sxs-lookup"><span data-stu-id="12759-142">-Scope</span></span>
<span data-ttu-id="12759-143">針對此 Cmdlet 所取得的作業，指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="12759-143">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12759-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12759-144">-DefaultProfile</span></span>
<span data-ttu-id="12759-145">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12759-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12759-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12759-146">CommonParameters</span></span>
<span data-ttu-id="12759-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12759-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12759-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12759-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12759-149">輸入</span><span class="sxs-lookup"><span data-stu-id="12759-149">INPUTS</span></span>

## <span data-ttu-id="12759-150">輸出</span><span class="sxs-lookup"><span data-stu-id="12759-150">OUTPUTS</span></span>

### <span data-ttu-id="12759-151">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="12759-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="12759-152">筆記</span><span class="sxs-lookup"><span data-stu-id="12759-152">NOTES</span></span>

## <span data-ttu-id="12759-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="12759-153">RELATED LINKS</span></span>

[<span data-ttu-id="12759-154">新-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="12759-154">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="12759-155">移除-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="12759-155">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="12759-156">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="12759-156">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


