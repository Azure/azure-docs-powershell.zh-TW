---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E42F05D0-28AD-4772-9F53-BCE6EFC698AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: bc7d44b87c1e371f0d0c065746dae991cff1cca8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967667"
---
# <span data-ttu-id="4cbab-101">New-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4cbab-101">New-AzureAutomationCredential</span></span>

## <span data-ttu-id="4cbab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cbab-102">SYNOPSIS</span></span>

<span data-ttu-id="4cbab-103">在自動化中建立認證。</span><span class="sxs-lookup"><span data-stu-id="4cbab-103">Creates a credential in Automation.</span></span>

## <span data-ttu-id="4cbab-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cbab-104">SYNTAX</span></span>

```
New-AzureAutomationCredential -Name <String> [-Description <String>] -Value <PSCredential>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4cbab-105">說明</span><span class="sxs-lookup"><span data-stu-id="4cbab-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4cbab-106">**新的-AzureAutomationCredential** Cmdlet 會在 Microsoft Azure 自動化中建立一個作為 **PSCredential** 物件的認證。</span><span class="sxs-lookup"><span data-stu-id="4cbab-106">The **New-AzureAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="4cbab-107">示例</span><span class="sxs-lookup"><span data-stu-id="4cbab-107">EXAMPLES</span></span>

### <span data-ttu-id="4cbab-108">範例1：建立認證</span><span class="sxs-lookup"><span data-stu-id="4cbab-108">Example 1: Create a credential</span></span>
```
PS C:\> $user = "MyDomain\MyUser"
PS C:\> $pw = ConvertTo-SecureString "PassWord!" -AsPlainText -Force
PS C:\> $cred = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $user, $pw
PS C:\> New-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential" -Value $cred
```

<span data-ttu-id="4cbab-109">這些命令會建立名為 MyCredential 的認證。</span><span class="sxs-lookup"><span data-stu-id="4cbab-109">These commands create a credential named MyCredential.</span></span>
<span data-ttu-id="4cbab-110">首先建立一個包含使用者名稱和密碼的認證物件。</span><span class="sxs-lookup"><span data-stu-id="4cbab-110">A credential object is first created that includes a username and password.</span></span>
<span data-ttu-id="4cbab-111">然後在最後一個命令中用來建立自動化認證。</span><span class="sxs-lookup"><span data-stu-id="4cbab-111">This is then used in the last command to create the Automation credential.</span></span>

## <span data-ttu-id="4cbab-112">參數</span><span class="sxs-lookup"><span data-stu-id="4cbab-112">PARAMETERS</span></span>

### <span data-ttu-id="4cbab-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4cbab-113">-AutomationAccountName</span></span>
<span data-ttu-id="4cbab-114">指定認證將儲存在其中的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4cbab-114">Specifies the name of the Automation account the credential will be stored in.</span></span>

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

### <span data-ttu-id="4cbab-115">-描述</span><span class="sxs-lookup"><span data-stu-id="4cbab-115">-Description</span></span>
<span data-ttu-id="4cbab-116">指定認證的描述。</span><span class="sxs-lookup"><span data-stu-id="4cbab-116">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="4cbab-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cbab-117">-Name</span></span>
<span data-ttu-id="4cbab-118">指定認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="4cbab-118">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="4cbab-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4cbab-119">-Profile</span></span>
<span data-ttu-id="4cbab-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4cbab-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4cbab-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="4cbab-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4cbab-122">-值</span><span class="sxs-lookup"><span data-stu-id="4cbab-122">-Value</span></span>
<span data-ttu-id="4cbab-123">將認證指定為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="4cbab-123">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cbab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbab-124">CommonParameters</span></span>
<span data-ttu-id="4cbab-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cbab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbab-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4cbab-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbab-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4cbab-127">INPUTS</span></span>

## <span data-ttu-id="4cbab-128">輸出</span><span class="sxs-lookup"><span data-stu-id="4cbab-128">OUTPUTS</span></span>

### <span data-ttu-id="4cbab-129">CredentialInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4cbab-129">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="4cbab-130">筆記</span><span class="sxs-lookup"><span data-stu-id="4cbab-130">NOTES</span></span>

## <span data-ttu-id="4cbab-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cbab-131">RELATED LINKS</span></span>

[<span data-ttu-id="4cbab-132">AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4cbab-132">Get-AzureAutomationCredential</span></span>](./Get-AzureAutomationCredential.md)

[<span data-ttu-id="4cbab-133">移除-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4cbab-133">Remove-AzureAutomationCredential</span></span>](./Remove-AzureAutomationCredential.md)

[<span data-ttu-id="4cbab-134">Set-AzureAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="4cbab-134">Set-AzureAutomationCredential</span></span>](./Set-AzureAutomationCredential.md)


