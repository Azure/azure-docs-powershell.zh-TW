---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967923"
---
# <span data-ttu-id="7688f-101">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7688f-101">Remove-AzureEnvironment</span></span>

## <span data-ttu-id="7688f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7688f-102">SYNOPSIS</span></span>
<span data-ttu-id="7688f-103">從 Windows PowerShell 刪除 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="7688f-103">Deletes an Azure environment from Windows PowerShell.</span></span>

## <span data-ttu-id="7688f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7688f-104">SYNTAX</span></span>

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7688f-105">說明</span><span class="sxs-lookup"><span data-stu-id="7688f-105">DESCRIPTION</span></span>
<span data-ttu-id="7688f-106">**AzureEnvironment** Cmdlet 會從您的漫遊設定檔中刪除 Azure 環境，讓 Windows PowerShell 找不到它。</span><span class="sxs-lookup"><span data-stu-id="7688f-106">The **Remove-AzureEnvironment** cmdlet deletes an Azure environment from your roaming profile so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="7688f-107">這個 Cmdlet 不會從 Microsoft Azure 刪除環境，或以任何方式變更實際的環境。</span><span class="sxs-lookup"><span data-stu-id="7688f-107">This cmdlet does not delete the environment from Microsoft Azure, or change the actual environment in any way.</span></span>

<span data-ttu-id="7688f-108">Azure 環境是獨立部署的 Microsoft Azure，例如針對全域 Azure 的 AzureCloud，以及由中國由世紀運營之 AzureChinaCloud 的 Azure。</span><span class="sxs-lookup"><span data-stu-id="7688f-108">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="7688f-109">您也可以使用 Azure Pack 和 WAPack Cmdlet，建立內部部署的 Azure 環境。</span><span class="sxs-lookup"><span data-stu-id="7688f-109">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="7688f-110">如需詳細資訊，請參閱 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="7688f-110">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

## <span data-ttu-id="7688f-111">示例</span><span class="sxs-lookup"><span data-stu-id="7688f-111">EXAMPLES</span></span>

### <span data-ttu-id="7688f-112">範例1：刪除環境</span><span class="sxs-lookup"><span data-stu-id="7688f-112">Example 1: Delete an environment</span></span>
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

<span data-ttu-id="7688f-113">這個命令會從 Windows PowerShell 中刪除 ContosoEnv 環境。</span><span class="sxs-lookup"><span data-stu-id="7688f-113">This command deletes the ContosoEnv environment from Windows PowerShell.</span></span>

### <span data-ttu-id="7688f-114">範例2：刪除多個環境</span><span class="sxs-lookup"><span data-stu-id="7688f-114">Example 2: Delete multiple environments</span></span>
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

<span data-ttu-id="7688f-115">這個命令會從 Windows PowerShell 中刪除名稱開頭為 "Contoso" 的環境。</span><span class="sxs-lookup"><span data-stu-id="7688f-115">This command deletes environments whose names begin with "Contoso" from Windows PowerShell.</span></span>

## <span data-ttu-id="7688f-116">參數</span><span class="sxs-lookup"><span data-stu-id="7688f-116">PARAMETERS</span></span>

### <span data-ttu-id="7688f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7688f-117">-Force</span></span>
<span data-ttu-id="7688f-118">取消確認提示。</span><span class="sxs-lookup"><span data-stu-id="7688f-118">Suppresses the confirmation prompt.</span></span>

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

### <span data-ttu-id="7688f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7688f-119">-Name</span></span>
<span data-ttu-id="7688f-120">指定要移除的環境名稱。</span><span class="sxs-lookup"><span data-stu-id="7688f-120">Specifies the name of the environment to remove.</span></span>
<span data-ttu-id="7688f-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="7688f-121">This parameter is required.</span></span>
<span data-ttu-id="7688f-122">這個參數值區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="7688f-122">This parameter value is case-sensitive.</span></span>
<span data-ttu-id="7688f-123">不允許通配字元。</span><span class="sxs-lookup"><span data-stu-id="7688f-123">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7688f-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7688f-124">-Profile</span></span>
<span data-ttu-id="7688f-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7688f-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="7688f-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7688f-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7688f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7688f-127">CommonParameters</span></span>
<span data-ttu-id="7688f-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7688f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7688f-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7688f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7688f-130">輸入</span><span class="sxs-lookup"><span data-stu-id="7688f-130">INPUTS</span></span>

### <span data-ttu-id="7688f-131">所有</span><span class="sxs-lookup"><span data-stu-id="7688f-131">None</span></span>
<span data-ttu-id="7688f-132">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7688f-132">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="7688f-133">輸出</span><span class="sxs-lookup"><span data-stu-id="7688f-133">OUTPUTS</span></span>

### <span data-ttu-id="7688f-134">None 或 System.object</span><span class="sxs-lookup"><span data-stu-id="7688f-134">None or System.Boolean</span></span>
<span data-ttu-id="7688f-135">如果您使用 *PassThru* 參數，這個 Cmdlet 會傳回布林值。</span><span class="sxs-lookup"><span data-stu-id="7688f-135">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="7688f-136">否則，它不會傳回任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7688f-136">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="7688f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7688f-137">NOTES</span></span>

## <span data-ttu-id="7688f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7688f-138">RELATED LINKS</span></span>

[<span data-ttu-id="7688f-139">附加 AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7688f-139">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="7688f-140">AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7688f-140">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="7688f-141">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7688f-141">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


