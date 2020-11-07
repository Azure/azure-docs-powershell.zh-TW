---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 9CED6E53-B65C-4D55-8AC7-9E8A8B143544
online version: ''
schema: 2.0.0
ms.openlocfilehash: da8f0e3bdc9e1cf573e9189e49feda85ee8c1b90
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967276"
---
# <span data-ttu-id="f12c6-101">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f12c6-101">Set-AzureAutomationModule</span></span>

## <span data-ttu-id="f12c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f12c6-102">SYNOPSIS</span></span>

<span data-ttu-id="f12c6-103">更新自動化中的模組。</span><span class="sxs-lookup"><span data-stu-id="f12c6-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="f12c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="f12c6-104">SYNTAX</span></span>

```
Set-AzureAutomationModule -Name <String> [-Tags <IDictionary>] [-ContentLinkUri <Uri>]
 [-ContentLinkVersion <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f12c6-105">說明</span><span class="sxs-lookup"><span data-stu-id="f12c6-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="f12c6-106">AzureAutomationModule Cmdlet 會匯入新版本的模組，或在 Azure 自動化中變更模組的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="f12c6-106">The **Set-AzureAutomationModule** cmdlet imports a new version of a module or changes the configuration of the module in Azure Automation.</span></span>

## <span data-ttu-id="f12c6-107">示例</span><span class="sxs-lookup"><span data-stu-id="f12c6-107">EXAMPLES</span></span>

### <span data-ttu-id="f12c6-108">範例1：更新模組</span><span class="sxs-lookup"><span data-stu-id="f12c6-108">Example 1: Update a module</span></span>
```
PS C:\> Set-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1"
```

<span data-ttu-id="f12c6-109">這個命令會將名為 ContosoModule 的現有模組更新版本，匯入到名為 Contoso17 的 Azure 自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="f12c6-109">This command imports an updated version of an existing module named ContosoModule into the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="f12c6-110">參數</span><span class="sxs-lookup"><span data-stu-id="f12c6-110">PARAMETERS</span></span>

### <span data-ttu-id="f12c6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f12c6-111">-AutomationAccountName</span></span>
<span data-ttu-id="f12c6-112">指定模組的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f12c6-112">Specifies the name of the Automation account with the module.</span></span>

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

### <span data-ttu-id="f12c6-113">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="f12c6-113">-ContentLinkUri</span></span>
<span data-ttu-id="f12c6-114">指定模組檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="f12c6-114">Specifies the path to the module file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f12c6-115">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="f12c6-115">-ContentLinkVersion</span></span>
<span data-ttu-id="f12c6-116">指定模組的版本。</span><span class="sxs-lookup"><span data-stu-id="f12c6-116">Specifies the version of the module.</span></span>

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

### <span data-ttu-id="f12c6-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="f12c6-117">-Name</span></span>
<span data-ttu-id="f12c6-118">指定模組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f12c6-118">Specifies the name of the module.</span></span>

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

### <span data-ttu-id="f12c6-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f12c6-119">-Profile</span></span>
<span data-ttu-id="f12c6-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f12c6-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f12c6-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f12c6-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f12c6-122">-標記</span><span class="sxs-lookup"><span data-stu-id="f12c6-122">-Tags</span></span>
<span data-ttu-id="f12c6-123">指定模組的標記。</span><span class="sxs-lookup"><span data-stu-id="f12c6-123">Specifies tags for the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f12c6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f12c6-124">CommonParameters</span></span>
<span data-ttu-id="f12c6-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f12c6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f12c6-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f12c6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f12c6-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f12c6-127">INPUTS</span></span>

### <span data-ttu-id="f12c6-128">[-Azure. 命令. Model. Module]</span><span class="sxs-lookup"><span data-stu-id="f12c6-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="f12c6-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f12c6-129">OUTPUTS</span></span>

## <span data-ttu-id="f12c6-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f12c6-130">NOTES</span></span>

## <span data-ttu-id="f12c6-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f12c6-131">RELATED LINKS</span></span>

[<span data-ttu-id="f12c6-132">AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f12c6-132">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="f12c6-133">新-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f12c6-133">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="f12c6-134">移除-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="f12c6-134">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)


