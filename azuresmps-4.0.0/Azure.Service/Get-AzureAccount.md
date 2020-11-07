---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 70ADAF16-BC52-47BF-A85A-A84DEACDA027
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2704dbdc308b9773452b05ceba24719f2e274132
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967122"
---
# <span data-ttu-id="50319-101">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="50319-101">Get-AzureAccount</span></span>

## <span data-ttu-id="50319-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50319-102">SYNOPSIS</span></span>
<span data-ttu-id="50319-103">取得可供 Azure PowerShell 使用的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="50319-103">Gets Azure accounts that are available to Azure PowerShell.</span></span>

## <span data-ttu-id="50319-104">句法</span><span class="sxs-lookup"><span data-stu-id="50319-104">SYNTAX</span></span>

```
Get-AzureAccount [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="50319-105">說明</span><span class="sxs-lookup"><span data-stu-id="50319-105">DESCRIPTION</span></span>
<span data-ttu-id="50319-106">**AzureAccount** Cmdlet 會取得適用于 Windows PowerShell 的 Azure 帳戶。</span><span class="sxs-lookup"><span data-stu-id="50319-106">The **Get-AzureAccount** cmdlet gets the Azure accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="50319-107">若要讓您的帳戶可供 Windows PowerShell 使用，請使用 **AzureAccount** 或 **Import PublishSettingsFile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50319-107">To make your accounts available to Windows PowerShell, use the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlets.</span></span>

## <span data-ttu-id="50319-108">示例</span><span class="sxs-lookup"><span data-stu-id="50319-108">EXAMPLES</span></span>

### <span data-ttu-id="50319-109">範例1：取得所有帳戶</span><span class="sxs-lookup"><span data-stu-id="50319-109">Example 1: Get all accounts</span></span>
```
PS C:\> Get-AzureAccount

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
contosotest1@outlook.com     {{ ActiveDirectoryTenantId = aaeabcde-386c-4466-bf70-794...
```

<span data-ttu-id="50319-110">這個命令會取得與指定使用者相關聯的所有帳戶。</span><span class="sxs-lookup"><span data-stu-id="50319-110">This command gets all accounts associated with the specified user.</span></span>

### <span data-ttu-id="50319-111">範例2：依名稱取得帳戶</span><span class="sxs-lookup"><span data-stu-id="50319-111">Example 2: Get an account by name</span></span>
```
PS C:\> Get-AzureAccount -Name contosoadmin@outlook.com

Name                         ActiveDirectories
----                         -----------------
contosoadmin@outlook.com     {{ ActiveDirectoryTenantId = abcde5cd-bcc3-441a-bd86-e6a...
```

<span data-ttu-id="50319-112">這個命令會取得 ContosoAdmin 帳戶。</span><span class="sxs-lookup"><span data-stu-id="50319-112">This command gets the ContosoAdmin account.</span></span>

## <span data-ttu-id="50319-113">參數</span><span class="sxs-lookup"><span data-stu-id="50319-113">PARAMETERS</span></span>

### <span data-ttu-id="50319-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="50319-114">-Name</span></span>
<span data-ttu-id="50319-115">只取得指定的帳號。</span><span class="sxs-lookup"><span data-stu-id="50319-115">Gets only the specified account.</span></span>
<span data-ttu-id="50319-116">預設值為所有可供 Windows PowerShell 使用的帳戶。</span><span class="sxs-lookup"><span data-stu-id="50319-116">The default is all accounts that are available to Windows PowerShell.</span></span>
<span data-ttu-id="50319-117">輸入帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="50319-117">Enter the account name.</span></span>
<span data-ttu-id="50319-118">[ **名稱** ] 值會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="50319-118">The **Name** value is case-sensitive.</span></span>
<span data-ttu-id="50319-119">不允許使用萬用字元。</span><span class="sxs-lookup"><span data-stu-id="50319-119">Wildcards are not permitted.</span></span>

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

### <span data-ttu-id="50319-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="50319-120">-Profile</span></span>
<span data-ttu-id="50319-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="50319-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="50319-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="50319-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="50319-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50319-123">CommonParameters</span></span>
<span data-ttu-id="50319-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50319-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50319-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="50319-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50319-126">輸入</span><span class="sxs-lookup"><span data-stu-id="50319-126">INPUTS</span></span>

### <span data-ttu-id="50319-127">所有</span><span class="sxs-lookup"><span data-stu-id="50319-127">None</span></span>
<span data-ttu-id="50319-128">您無法將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50319-128">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="50319-129">輸出</span><span class="sxs-lookup"><span data-stu-id="50319-129">OUTPUTS</span></span>

### <span data-ttu-id="50319-130">所有</span><span class="sxs-lookup"><span data-stu-id="50319-130">None</span></span>
<span data-ttu-id="50319-131">這個 Cmdlet 不會傳回任何輸出。</span><span class="sxs-lookup"><span data-stu-id="50319-131">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="50319-132">筆記</span><span class="sxs-lookup"><span data-stu-id="50319-132">NOTES</span></span>

## <span data-ttu-id="50319-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="50319-133">RELATED LINKS</span></span>

[<span data-ttu-id="50319-134">附加 AzureAccount</span><span class="sxs-lookup"><span data-stu-id="50319-134">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="50319-135">AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="50319-135">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="50319-136">匯入-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="50319-136">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="50319-137">移除-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="50319-137">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


