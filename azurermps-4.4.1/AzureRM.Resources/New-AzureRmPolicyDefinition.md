---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: 5140219c5392a7fb9c727998ae248d600edfde23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453292"
---
# <span data-ttu-id="50c8f-101">New-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="50c8f-101">New-AzureRmPolicyDefinition</span></span>

## <span data-ttu-id="50c8f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="50c8f-103">建立原則定義。</span><span class="sxs-lookup"><span data-stu-id="50c8f-103">Creates a policy definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50c8f-104">句法</span><span class="sxs-lookup"><span data-stu-id="50c8f-104">SYNTAX</span></span>

```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="50c8f-105">說明</span><span class="sxs-lookup"><span data-stu-id="50c8f-105">DESCRIPTION</span></span>
<span data-ttu-id="50c8f-106">**AzureRmPolicyDefinition** Cmdlet 會建立原則定義，其中包含 JavaScript) 格式 (JSON 物件符號中的原則規則。</span><span class="sxs-lookup"><span data-stu-id="50c8f-106">The **New-AzureRmPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="50c8f-107">示例</span><span class="sxs-lookup"><span data-stu-id="50c8f-107">EXAMPLES</span></span>

### <span data-ttu-id="50c8f-108">範例1：使用原則檔建立原則定義</span><span class="sxs-lookup"><span data-stu-id="50c8f-108">Example 1: Create a policy definition by using a policy file</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -Policy C:\VMPolicy.json
```

<span data-ttu-id="50c8f-109">這個命令會建立一個名為 VMPolicyDefinition 的原則定義，其中包含 C:\VMPolicy.json 中指定的原則規則。</span><span class="sxs-lookup"><span data-stu-id="50c8f-109">This command creates a policy definition named VMPolicyDefinition that contains the policy rule specified in C:\VMPolicy.json.</span></span>

### <span data-ttu-id="50c8f-110">範例2：直接建立原則定義</span><span class="sxs-lookup"><span data-stu-id="50c8f-110">Example 2: Create a policy definition inline</span></span>
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -DisplayName "Virtual Machine policy definition" -Policy "{""if"":{""source"":""action"",""equals"":""Microsoft.Compute/virtualMachines/write""},""then"":{""effect"":""deny""}}"
```

<span data-ttu-id="50c8f-111">這個命令會建立名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="50c8f-111">This command creates a policy definition named VMPolicyDefinition.</span></span>
<span data-ttu-id="50c8f-112">該命令會將原則指定為有效 JSON 格式的字串。</span><span class="sxs-lookup"><span data-stu-id="50c8f-112">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="50c8f-113">參數</span><span class="sxs-lookup"><span data-stu-id="50c8f-113">PARAMETERS</span></span>

### <span data-ttu-id="50c8f-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="50c8f-114">-ApiVersion</span></span>
<span data-ttu-id="50c8f-115">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="50c8f-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="50c8f-116">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="50c8f-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="50c8f-117">-描述</span><span class="sxs-lookup"><span data-stu-id="50c8f-117">-Description</span></span>
<span data-ttu-id="50c8f-118">指定原則定義的描述。</span><span class="sxs-lookup"><span data-stu-id="50c8f-118">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="50c8f-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="50c8f-119">-DisplayName</span></span>
<span data-ttu-id="50c8f-120">指定原則定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="50c8f-120">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="50c8f-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="50c8f-121">-InformationAction</span></span>
<span data-ttu-id="50c8f-122">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="50c8f-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="50c8f-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="50c8f-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="50c8f-124">持續</span><span class="sxs-lookup"><span data-stu-id="50c8f-124">Continue</span></span>
- <span data-ttu-id="50c8f-125">理會</span><span class="sxs-lookup"><span data-stu-id="50c8f-125">Ignore</span></span>
- <span data-ttu-id="50c8f-126">看</span><span class="sxs-lookup"><span data-stu-id="50c8f-126">Inquire</span></span>
- <span data-ttu-id="50c8f-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="50c8f-127">SilentlyContinue</span></span>
- <span data-ttu-id="50c8f-128">停止</span><span class="sxs-lookup"><span data-stu-id="50c8f-128">Stop</span></span>
- <span data-ttu-id="50c8f-129">封存</span><span class="sxs-lookup"><span data-stu-id="50c8f-129">Suspend</span></span>

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

### <span data-ttu-id="50c8f-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="50c8f-130">-InformationVariable</span></span>
<span data-ttu-id="50c8f-131">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="50c8f-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="50c8f-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="50c8f-132">-Name</span></span>
<span data-ttu-id="50c8f-133">指定原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="50c8f-133">Specifies a name for the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50c8f-134">-參數</span><span class="sxs-lookup"><span data-stu-id="50c8f-134">-Parameter</span></span>
<span data-ttu-id="50c8f-135">原則定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="50c8f-135">The parameters declaration for policy definition.</span></span> <span data-ttu-id="50c8f-136">這可以是包含參數宣告之檔案名的路徑，或是參數宣告（字串）。</span><span class="sxs-lookup"><span data-stu-id="50c8f-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="50c8f-137">-原則</span><span class="sxs-lookup"><span data-stu-id="50c8f-137">-Policy</span></span>
<span data-ttu-id="50c8f-138">指定原則定義的原則規則。</span><span class="sxs-lookup"><span data-stu-id="50c8f-138">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="50c8f-139">您可以指定 json 檔案的路徑，或是包含 JSON 格式之原則的字串。</span><span class="sxs-lookup"><span data-stu-id="50c8f-139">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50c8f-140">-預先</span><span class="sxs-lookup"><span data-stu-id="50c8f-140">-Pre</span></span>
<span data-ttu-id="50c8f-141">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="50c8f-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="50c8f-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c8f-142">-DefaultProfile</span></span>
<span data-ttu-id="50c8f-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="50c8f-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50c8f-144">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="50c8f-144">-Metadata</span></span>
<span data-ttu-id="50c8f-145">原則定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="50c8f-145">The metadata for policy definition.</span></span> <span data-ttu-id="50c8f-146">這可以是包含中繼資料之檔案名的路徑，或以字串形式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="50c8f-146">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="50c8f-147">模式</span><span class="sxs-lookup"><span data-stu-id="50c8f-147">-Mode</span></span>
<span data-ttu-id="50c8f-148">原則定義的模式。</span><span class="sxs-lookup"><span data-stu-id="50c8f-148">The mode of the policy definition.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50c8f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c8f-149">CommonParameters</span></span>
<span data-ttu-id="50c8f-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50c8f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c8f-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="50c8f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c8f-152">輸入</span><span class="sxs-lookup"><span data-stu-id="50c8f-152">INPUTS</span></span>

## <span data-ttu-id="50c8f-153">輸出</span><span class="sxs-lookup"><span data-stu-id="50c8f-153">OUTPUTS</span></span>

### <span data-ttu-id="50c8f-154">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="50c8f-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="50c8f-155">筆記</span><span class="sxs-lookup"><span data-stu-id="50c8f-155">NOTES</span></span>

## <span data-ttu-id="50c8f-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="50c8f-156">RELATED LINKS</span></span>

[<span data-ttu-id="50c8f-157">AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="50c8f-157">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="50c8f-158">移除-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="50c8f-158">Remove-AzureRmPolicyDefinition</span></span>](./Remove-AzureRmPolicyDefinition.md)

[<span data-ttu-id="50c8f-159">Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="50c8f-159">Set-AzureRmPolicyDefinition</span></span>](./Set-AzureRmPolicyDefinition.md)


