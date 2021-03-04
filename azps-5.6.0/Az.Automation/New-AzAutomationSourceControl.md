---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSourceControl.md
ms.openlocfilehash: d9fbbed1beb67ce1bc8732cb5641c78705fd6a5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903046"
---
# <span data-ttu-id="af2ec-101">New-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="af2ec-101">New-AzAutomationSourceControl</span></span>

## <span data-ttu-id="af2ec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="af2ec-102">SYNOPSIS</span></span>
<span data-ttu-id="af2ec-103">建立自動化原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="af2ec-103">Creates an A Automation source control.</span></span>

## <span data-ttu-id="af2ec-104">語法</span><span class="sxs-lookup"><span data-stu-id="af2ec-104">SYNTAX</span></span>

```
New-AzAutomationSourceControl -Name <String> -RepoUrl <Uri> -SourceType <String> -AccessToken <SecureString>
 -FolderPath <String> [-Branch <String>] [-Description <String>] [-EnableAutoSync] [-DoNotPublishRunbook]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af2ec-105">描述</span><span class="sxs-lookup"><span data-stu-id="af2ec-105">DESCRIPTION</span></span>
<span data-ttu-id="af2ec-106">此New-AzAutomationSourceControl Cmdlet 會建立一個組塊，將 Azure 自動化帳戶與 VSTS TFVC、VSTS Git 或 GitHub 連結。</span><span class="sxs-lookup"><span data-stu-id="af2ec-106">The New-AzAutomationSourceControl cmdlet creates a configuration to link my Azure Automation account with my VSTS TFVC, VSTS Git or GitHub.</span></span>

## <span data-ttu-id="af2ec-107">例子</span><span class="sxs-lookup"><span data-stu-id="af2ec-107">EXAMPLES</span></span>

### <span data-ttu-id="af2ec-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="af2ec-108">Example 1</span></span>
<span data-ttu-id="af2ec-109">建立原始程式碼管理組，將 Azure 自動化帳戶與 VSTS TFVC 專案連結。</span><span class="sxs-lookup"><span data-stu-id="af2ec-109">Create a source control configuration to link my Azure Automation account with my VSTS TFVC project.</span></span> <span data-ttu-id="af2ec-110">TFVC 專案沒有分支，因此未指定分支參數。</span><span class="sxs-lookup"><span data-stu-id="af2ec-110">TFVC projects do not have branches, and therefore, the Branch parameter is not specified.</span></span>

```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSNative" `
                                           -RepoUrl "https://dev.azure.com/<accountname>/<adoprojectname>/_git/<repositoryname>" `
                                           -SourceType "VsoTfvc" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name        SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----        ---------- ------ ---------- -------- -------------- -------
VSTSNative  VsoTfvc            /Runbooks True     True           https://dev.azure.com/<accountname>/<adopro...
```

### <span data-ttu-id="af2ec-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="af2ec-111">Example 2</span></span>
<span data-ttu-id="af2ec-112">建立原始程式碼管理組，將 Azure 自動化帳戶與 VSTS Git 專案連結。</span><span class="sxs-lookup"><span data-stu-id="af2ec-112">Create a source control configuration to link my Azure Automation account with my VSTS Git project.</span></span>


```powershell
PS C:\> # VSTS Personal access token
PS C:\> $token = "vppmrabbs65axamofglyo66rjg6reddaa7xxgvaddd5555aaaaddxzbmma"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "VSTSGit" `
                                           -RepoUrl "https://dev.azure.com/<accountname>/<adoprojectname>/_git/<repositoryname>" `
                                           -SourceType "VsoGit" `
                                           -Branch "Development" `
                                           -FolderPath "/" `
                                           -AccessToken $accessToken

Name    SourceType Branch      FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------      ---------- -------- -------------- -------
VSTSGit VsoGit     Development /          True     True           https://dev.azure.com/<accountname>/<adopro...
```

### <span data-ttu-id="af2ec-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="af2ec-113">Example 3</span></span>
<span data-ttu-id="af2ec-114">建立原始程式碼管理組配置，將 Azure 自動化帳戶與 GitHub 專案連結。</span><span class="sxs-lookup"><span data-stu-id="af2ec-114">Create a source control configuration to link my Azure Automation account with my GitHub project.</span></span>


```powershell
PS C:\> # GitHub access token
PS C:\> $token = "68b08011223aac8bdd3388913a44rrsaa84fdf"
PS C:\> $accessToken = ConvertTo-SecureString -String $token -AsPlainText -Force 
PS C:\> New-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name  "GitHub1" `
                                           -RepoUrl "https://github.com/Contoso/TestSourceControl.git" `
                                           -SourceType "GitHub" `
                                           -Branch "master" `
                                           -FolderPath "/Runbooks" `
                                           -AccessToken $accessToken

Name    SourceType Branch FolderPath AutoSync PublishRunbook RepoUrl
----    ---------- ------ ---------- -------- -------------- -------
GitHub1 GitHub     master /Runbooks  True     True           https://github.com/Contoso/TestSourceControl...
```

## <span data-ttu-id="af2ec-115">參數</span><span class="sxs-lookup"><span data-stu-id="af2ec-115">PARAMETERS</span></span>

### <span data-ttu-id="af2ec-116">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="af2ec-116">-AccessToken</span></span>
<span data-ttu-id="af2ec-117">原始程式碼管理存取權杖。</span><span class="sxs-lookup"><span data-stu-id="af2ec-117">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2ec-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="af2ec-118">-AutomationAccountName</span></span>
<span data-ttu-id="af2ec-119">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="af2ec-119">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2ec-120">-分支</span><span class="sxs-lookup"><span data-stu-id="af2ec-120">-Branch</span></span>
<span data-ttu-id="af2ec-121">原始程式碼管理分支。</span><span class="sxs-lookup"><span data-stu-id="af2ec-121">The source control branch.</span></span>

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

### <span data-ttu-id="af2ec-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af2ec-122">-DefaultProfile</span></span>
<span data-ttu-id="af2ec-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="af2ec-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af2ec-124">-描述</span><span class="sxs-lookup"><span data-stu-id="af2ec-124">-Description</span></span>
<span data-ttu-id="af2ec-125">原始程式碼管理描述。</span><span class="sxs-lookup"><span data-stu-id="af2ec-125">The source control description.</span></span>

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

### <span data-ttu-id="af2ec-126">-DoNotPublishRunbook</span><span class="sxs-lookup"><span data-stu-id="af2ec-126">-DoNotPublishRunbook</span></span>
<span data-ttu-id="af2ec-127">原始程式碼的 publishRunbook 屬性。</span><span class="sxs-lookup"><span data-stu-id="af2ec-127">The publishRunbook property of the source control.</span></span>
<span data-ttu-id="af2ec-128">如果 DoNotPublishRunbook 已設定，這表示使用者 runbooks 會以'草稿'方式輸入。</span><span class="sxs-lookup"><span data-stu-id="af2ec-128">If DoNotPublishRunbook is set, this means that user runbooks will be imported as 'Draft'.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2ec-129">-EnableAutoSync</span><span class="sxs-lookup"><span data-stu-id="af2ec-129">-EnableAutoSync</span></span>
<span data-ttu-id="af2ec-130">來源控制項的 autoSync 屬性。</span><span class="sxs-lookup"><span data-stu-id="af2ec-130">The autoSync property for the source control.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2ec-131">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="af2ec-131">-FolderPath</span></span>
<span data-ttu-id="af2ec-132">原始程式碼管理資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="af2ec-132">The source control folder path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2ec-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="af2ec-133">-Name</span></span>
<span data-ttu-id="af2ec-134">原始程式碼管理名稱。</span><span class="sxs-lookup"><span data-stu-id="af2ec-134">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2ec-135">-RepoUrl</span><span class="sxs-lookup"><span data-stu-id="af2ec-135">-RepoUrl</span></span>
<span data-ttu-id="af2ec-136">原始程式碼管理 Repo URL。</span><span class="sxs-lookup"><span data-stu-id="af2ec-136">The source control repo url.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2ec-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af2ec-137">-ResourceGroupName</span></span>
<span data-ttu-id="af2ec-138">資源組名。</span><span class="sxs-lookup"><span data-stu-id="af2ec-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af2ec-139">-SourceType</span><span class="sxs-lookup"><span data-stu-id="af2ec-139">-SourceType</span></span>
<span data-ttu-id="af2ec-140">原始程式碼管理類型。</span><span class="sxs-lookup"><span data-stu-id="af2ec-140">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2ec-141">-確認</span><span class="sxs-lookup"><span data-stu-id="af2ec-141">-Confirm</span></span>
<span data-ttu-id="af2ec-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="af2ec-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2ec-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af2ec-143">-WhatIf</span></span>
<span data-ttu-id="af2ec-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af2ec-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af2ec-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af2ec-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af2ec-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af2ec-146">CommonParameters</span></span>
<span data-ttu-id="af2ec-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="af2ec-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af2ec-148">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="af2ec-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af2ec-149">輸入</span><span class="sxs-lookup"><span data-stu-id="af2ec-149">INPUTS</span></span>

### <span data-ttu-id="af2ec-150">System.String</span><span class="sxs-lookup"><span data-stu-id="af2ec-150">System.String</span></span>

## <span data-ttu-id="af2ec-151">輸出</span><span class="sxs-lookup"><span data-stu-id="af2ec-151">OUTPUTS</span></span>

### <span data-ttu-id="af2ec-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="af2ec-152">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="af2ec-153">筆記</span><span class="sxs-lookup"><span data-stu-id="af2ec-153">NOTES</span></span>

## <span data-ttu-id="af2ec-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="af2ec-154">RELATED LINKS</span></span>
