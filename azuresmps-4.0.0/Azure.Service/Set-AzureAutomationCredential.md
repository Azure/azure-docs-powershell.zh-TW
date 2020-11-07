---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C92B4B70-4342-4219-80D3-FB79BDC171A3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 16fbdf1a0a63fb5a75aa7bc200036a7332ea15f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967277"
---
# <span data-ttu-id="2ceac-101">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2ceac-101">Set-AzureAutomationCredential</span></span>

## <span data-ttu-id="2ceac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ceac-102">SYNOPSIS</span></span>

<span data-ttu-id="2ceac-103">在自動化中修改認證。</span><span class="sxs-lookup"><span data-stu-id="2ceac-103">Modifies a credential in Automation.</span></span>

## <span data-ttu-id="2ceac-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ceac-104">SYNTAX</span></span>

```
Set-AzureAutomationCredential -Name <String> [-Description <String>] [-Value <PSCredential>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2ceac-105">說明</span><span class="sxs-lookup"><span data-stu-id="2ceac-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="2ceac-106">**AzureAutomationCredential** Cmdlet 會在 Microsoft Azure 自動化中修改作為 **PSCredential** 物件的認證。</span><span class="sxs-lookup"><span data-stu-id="2ceac-106">The **Set-AzureAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="2ceac-107">示例</span><span class="sxs-lookup"><span data-stu-id="2ceac-107">EXAMPLES</span></span>

### <span data-ttu-id="2ceac-108">範例1：更新認證</span><span class="sxs-lookup"><span data-stu-id="2ceac-108">Example 1: Update a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contos17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="2ceac-109">這些命令會更新名為 MyCredential 的現有認證。</span><span class="sxs-lookup"><span data-stu-id="2ceac-109">These commands update an existing credential named MyCredential.</span></span>
<span data-ttu-id="2ceac-110">首先建立一個包含使用者名稱和密碼的認證物件。</span><span class="sxs-lookup"><span data-stu-id="2ceac-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="2ceac-111">然後在最後一個命令中用來更新自動化認證。</span><span class="sxs-lookup"><span data-stu-id="2ceac-111">This is then used in the last command to update the automation credential.</span></span>

## <span data-ttu-id="2ceac-112">參數</span><span class="sxs-lookup"><span data-stu-id="2ceac-112">PARAMETERS</span></span>

### <span data-ttu-id="2ceac-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2ceac-113">-AutomationAccountName</span></span>
<span data-ttu-id="2ceac-114">指定含認證之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ceac-114">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="2ceac-115">-描述</span><span class="sxs-lookup"><span data-stu-id="2ceac-115">-Description</span></span>
<span data-ttu-id="2ceac-116">指定認證的描述。</span><span class="sxs-lookup"><span data-stu-id="2ceac-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="2ceac-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ceac-117">-Name</span></span>
<span data-ttu-id="2ceac-118">指定認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ceac-118">Specifies the name of the credential.</span></span>

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

### <span data-ttu-id="2ceac-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="2ceac-119">-Profile</span></span>
<span data-ttu-id="2ceac-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="2ceac-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2ceac-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="2ceac-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ceac-122">-值</span><span class="sxs-lookup"><span data-stu-id="2ceac-122">-Value</span></span>
<span data-ttu-id="2ceac-123">將認證指定為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="2ceac-123">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="2ceac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ceac-124">CommonParameters</span></span>
<span data-ttu-id="2ceac-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ceac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ceac-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2ceac-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ceac-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2ceac-127">INPUTS</span></span>

## <span data-ttu-id="2ceac-128">輸出</span><span class="sxs-lookup"><span data-stu-id="2ceac-128">OUTPUTS</span></span>

### <span data-ttu-id="2ceac-129">CredentialInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="2ceac-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="2ceac-130">筆記</span><span class="sxs-lookup"><span data-stu-id="2ceac-130">NOTES</span></span>

## <span data-ttu-id="2ceac-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ceac-131">RELATED LINKS</span></span>

[<span data-ttu-id="2ceac-132">AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2ceac-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="2ceac-133">新-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2ceac-133">New-AzureAutomationCredential</span></span>](./New-AzureAutomationCredential.md)

[<span data-ttu-id="2ceac-134">移除-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="2ceac-134">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)


