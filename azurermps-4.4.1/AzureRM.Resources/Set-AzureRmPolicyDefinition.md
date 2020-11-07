---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmPolicyDefinition.md
ms.openlocfilehash: 2404c0f2dc6c357503f23e7ed509f1c58c352c8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625682"
---
# <span data-ttu-id="4c782-101">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4c782-101">Set-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="4c782-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c782-102">SYNOPSIS</span></span>
<span data-ttu-id="4c782-103">修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="4c782-103">Modifies a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c782-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c782-104">SYNTAX</span></span>

### <span data-ttu-id="4c782-105">原則定義名稱參數已設定。</span><span class="sxs-lookup"><span data-stu-id="4c782-105">The policy definition name parameter set.</span></span> <span data-ttu-id="4c782-106"> (預設) </span><span class="sxs-lookup"><span data-stu-id="4c782-106">(Default)</span></span>
```
Set-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4c782-107">已設定原則定義識別碼參數。</span><span class="sxs-lookup"><span data-stu-id="4c782-107">The policy definition Id parameter set.</span></span>
```
Set-AzureRmPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4c782-108">說明</span><span class="sxs-lookup"><span data-stu-id="4c782-108">DESCRIPTION</span></span>
<span data-ttu-id="4c782-109">**AzureRmPolicyDefinition** Cmdlet 會修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="4c782-109">The **Set-AzureRmPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="4c782-110">示例</span><span class="sxs-lookup"><span data-stu-id="4c782-110">EXAMPLES</span></span>

### <span data-ttu-id="4c782-111">範例1：更新原則定義的描述</span><span class="sxs-lookup"><span data-stu-id="4c782-111">Example 1: Update the description of a policy definition</span></span>
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
PS C:\> Set-AzureRmPolicyDefinition -Id $Policy.ResourceId -Description "Updated policy to not allow virtual machine creation"
```

<span data-ttu-id="4c782-112">第一個命令會使用 Get-AzureRmPolicyDefinition Cmdlet 來取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="4c782-112">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="4c782-113">該命令會將該物件儲存在 $PolicyDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="4c782-113">The command stores that object in the $PolicyDefinition variable.</span></span>

<span data-ttu-id="4c782-114">第二個命令會更新 $PolicyDefinition 的 **ResourceId** 屬性所識別之原則定義的描述。</span><span class="sxs-lookup"><span data-stu-id="4c782-114">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="4c782-115">參數</span><span class="sxs-lookup"><span data-stu-id="4c782-115">PARAMETERS</span></span>

### <span data-ttu-id="4c782-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4c782-116">-ApiVersion</span></span>
<span data-ttu-id="4c782-117">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4c782-117">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4c782-118">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="4c782-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4c782-119">-描述</span><span class="sxs-lookup"><span data-stu-id="4c782-119">-Description</span></span>
<span data-ttu-id="4c782-120">指定原則定義的新描述。</span><span class="sxs-lookup"><span data-stu-id="4c782-120">Specifies a new description for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c782-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4c782-121">-DisplayName</span></span>
<span data-ttu-id="4c782-122">指定原則定義的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4c782-122">Specifies a new display name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c782-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="4c782-123">-Id</span></span>
<span data-ttu-id="4c782-124">指定此 Cmdlet 所修改之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c782-124">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c782-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4c782-125">-InformationAction</span></span>
<span data-ttu-id="4c782-126">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="4c782-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4c782-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4c782-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4c782-128">持續</span><span class="sxs-lookup"><span data-stu-id="4c782-128">Continue</span></span>
- <span data-ttu-id="4c782-129">理會</span><span class="sxs-lookup"><span data-stu-id="4c782-129">Ignore</span></span>
- <span data-ttu-id="4c782-130">看</span><span class="sxs-lookup"><span data-stu-id="4c782-130">Inquire</span></span>
- <span data-ttu-id="4c782-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4c782-131">SilentlyContinue</span></span>
- <span data-ttu-id="4c782-132">停止</span><span class="sxs-lookup"><span data-stu-id="4c782-132">Stop</span></span>
- <span data-ttu-id="4c782-133">封存</span><span class="sxs-lookup"><span data-stu-id="4c782-133">Suspend</span></span>

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

### <span data-ttu-id="4c782-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4c782-134">-InformationVariable</span></span>
<span data-ttu-id="4c782-135">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="4c782-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4c782-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="4c782-136">-Name</span></span>
<span data-ttu-id="4c782-137">指定此 Cmdlet 所修改之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c782-137">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c782-138">-原則</span><span class="sxs-lookup"><span data-stu-id="4c782-138">-Policy</span></span>
<span data-ttu-id="4c782-139">指定原則定義的新原則規則。</span><span class="sxs-lookup"><span data-stu-id="4c782-139">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="4c782-140">您可以指定 json 檔案的路徑，或是包含 JavaScript 物件符號 (JSON) 格式之原則的字串。</span><span class="sxs-lookup"><span data-stu-id="4c782-140">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c782-141">-預先</span><span class="sxs-lookup"><span data-stu-id="4c782-141">-Pre</span></span>
<span data-ttu-id="4c782-142">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4c782-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4c782-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c782-143">-DefaultProfile</span></span>
<span data-ttu-id="4c782-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c782-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c782-145">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="4c782-145">-Metadata</span></span>
<span data-ttu-id="4c782-146">原則定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="4c782-146">The metadata for policy definition.</span></span> <span data-ttu-id="4c782-147">這可以是包含中繼資料之檔案名的路徑，或以字串形式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="4c782-147">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c782-148">-參數</span><span class="sxs-lookup"><span data-stu-id="4c782-148">-Parameter</span></span>
<span data-ttu-id="4c782-149">原則定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="4c782-149">The parameters declaration for policy definition.</span></span> <span data-ttu-id="4c782-150">這可以是包含參數宣告之檔案名或 uri 的路徑，或是參數宣告（字串）。</span><span class="sxs-lookup"><span data-stu-id="4c782-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c782-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c782-151">CommonParameters</span></span>
<span data-ttu-id="4c782-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c782-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c782-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4c782-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c782-154">輸入</span><span class="sxs-lookup"><span data-stu-id="4c782-154">INPUTS</span></span>

## <span data-ttu-id="4c782-155">輸出</span><span class="sxs-lookup"><span data-stu-id="4c782-155">OUTPUTS</span></span>

### <span data-ttu-id="4c782-156">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="4c782-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4c782-157">筆記</span><span class="sxs-lookup"><span data-stu-id="4c782-157">NOTES</span></span>

## <span data-ttu-id="4c782-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c782-158">RELATED LINKS</span></span>

[<span data-ttu-id="4c782-159">AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4c782-159">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="4c782-160">新-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4c782-160">New-AzureRmPolicyDefinition</span></span>](./New-AzureRmPolicyDefinition.md)

[<span data-ttu-id="4c782-161">移除-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4c782-161">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)


