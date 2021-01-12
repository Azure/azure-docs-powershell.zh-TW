---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110473"
---
# <span data-ttu-id="fc5b1-101">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="fc5b1-101">New-AzureWebsite</span></span>

## <span data-ttu-id="fc5b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc5b1-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5b1-103">在 Azure 中建立要執行的新網站。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-103">Create a new website to run in Azure.</span></span>

## <span data-ttu-id="fc5b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc5b1-104">SYNTAX</span></span>

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fc5b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="fc5b1-105">DESCRIPTION</span></span>
<span data-ttu-id="fc5b1-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="fc5b1-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="fc5b1-108">這個 Cmdlet 會建立新的網站，以在 Azure 中執行，並準備透過 GitHub 進行部署。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-108">The cmdlet creates a new website to run in Azure and prepares for deployment through GitHub.</span></span>

## <span data-ttu-id="fc5b1-109">示例</span><span class="sxs-lookup"><span data-stu-id="fc5b1-109">EXAMPLES</span></span>

### <span data-ttu-id="fc5b1-110">範例1：使用 Git 建立新的網站</span><span class="sxs-lookup"><span data-stu-id="fc5b1-110">Example 1: Create a new website with Git</span></span>
```
PS C:\> New-AzureWebsite mySite -Git
```

<span data-ttu-id="fc5b1-111">這個範例會在 Azure 中建立新的網站，以及用來將檔案部署至新網站的本機 Git 儲存庫。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-111">This example creates a new website in Azure and a local Git repository to use for deploying files to the new website.</span></span>

### <span data-ttu-id="fc5b1-112">範例2：建立與 GitHub 整合的網站</span><span class="sxs-lookup"><span data-stu-id="fc5b1-112">Example 2: Create website integrated with GitHub</span></span>
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

<span data-ttu-id="fc5b1-113">這個範例會建立連結至 GitHub 知識庫的新網站，名為 [我的帳戶/myrepo]。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-113">This example creates a new website linked to a GitHub repository named myaccount/myrepo.</span></span>
<span data-ttu-id="fc5b1-114">將提交至 GitHub 儲存庫的專案會推送至 Azure 中的網站。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-114">Commits to the GitHub repository are pushed to the website in Azure.</span></span>

## <span data-ttu-id="fc5b1-115">參數</span><span class="sxs-lookup"><span data-stu-id="fc5b1-115">PARAMETERS</span></span>

### <span data-ttu-id="fc5b1-116">-Git</span><span class="sxs-lookup"><span data-stu-id="fc5b1-116">-Git</span></span>
<span data-ttu-id="fc5b1-117">設定本機 Git 儲存庫並將其連結至網站。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-117">Sets up a local Git repository and links it to the website.</span></span>
<span data-ttu-id="fc5b1-118">如果已指定，此參數會在本機目錄中設定 Git 儲存庫，並新增一個名為「azure ' 的遠端知識庫，並連結至 Azure 中的網站。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-118">If specified, this parameter sets up a Git repository in the local directory and add a remote repository named 'azure' that links to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc5b1-119">-GitHub</span><span class="sxs-lookup"><span data-stu-id="fc5b1-119">-GitHub</span></span>
<span data-ttu-id="fc5b1-120">表示此 Cmdlet 會將新的網站連結至現有的 GitHub 儲存庫。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-120">Indicates that this cmdlet links the new website to an existing GitHub repository.</span></span>
<span data-ttu-id="fc5b1-121">提交至 Giuthub 知識庫的功能會推送至 Azure 中的網站。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-121">Commits to the Giuthub repository are pushed to the website in Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc5b1-122">-GitHubCredentials</span><span class="sxs-lookup"><span data-stu-id="fc5b1-122">-GitHubCredentials</span></span>
<span data-ttu-id="fc5b1-123">指定要連線至 GitHub 的使用者名稱和密碼認證。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-123">Specifies the user name and password credentials to connect to GitHub.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc5b1-124">-GitHubRepository</span><span class="sxs-lookup"><span data-stu-id="fc5b1-124">-GitHubRepository</span></span>
<span data-ttu-id="fc5b1-125">指定 GitHub 儲存庫的完整名稱以連結至此網站。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-125">Specifies the full name of the GitHub repository to link to this website.</span></span>
<span data-ttu-id="fc5b1-126">例如， `myaccount/myrepo` 。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-126">For example, `myaccount/myrepo`.</span></span>

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

### <span data-ttu-id="fc5b1-127">-Hostname</span><span class="sxs-lookup"><span data-stu-id="fc5b1-127">-Hostname</span></span>
<span data-ttu-id="fc5b1-128">指定新網站的替代主機名稱。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-128">Specifies an alternative host name for the new website.</span></span>

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

### <span data-ttu-id="fc5b1-129">-位置</span><span class="sxs-lookup"><span data-stu-id="fc5b1-129">-Location</span></span>
<span data-ttu-id="fc5b1-130">指定您要部署網站之資料中心的位置。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-130">Specifies the location of the data center where you want to deploy the website.</span></span>

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

### <span data-ttu-id="fc5b1-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc5b1-131">-Name</span></span>
<span data-ttu-id="fc5b1-132">指定網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-132">Specifies a name for the website.</span></span>

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

### <span data-ttu-id="fc5b1-133">-設定檔</span><span class="sxs-lookup"><span data-stu-id="fc5b1-133">-Profile</span></span>
<span data-ttu-id="fc5b1-134">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fc5b1-135">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc5b1-136">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="fc5b1-136">-PublishingUsername</span></span>
<span data-ttu-id="fc5b1-137">指定您在使用 Git 部署的 Azure 入口網站中指定的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-137">Specifies the user name you have specified in the Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="fc5b1-138">-槽</span><span class="sxs-lookup"><span data-stu-id="fc5b1-138">-Slot</span></span>
<span data-ttu-id="fc5b1-139">指定網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-139">Specifies a slot name for the website.</span></span>

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

### <span data-ttu-id="fc5b1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5b1-140">CommonParameters</span></span>
<span data-ttu-id="fc5b1-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5b1-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc5b1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5b1-143">輸入</span><span class="sxs-lookup"><span data-stu-id="fc5b1-143">INPUTS</span></span>

## <span data-ttu-id="fc5b1-144">輸出</span><span class="sxs-lookup"><span data-stu-id="fc5b1-144">OUTPUTS</span></span>

## <span data-ttu-id="fc5b1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="fc5b1-145">NOTES</span></span>

## <span data-ttu-id="fc5b1-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc5b1-146">RELATED LINKS</span></span>

[<span data-ttu-id="fc5b1-147">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="fc5b1-147">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


