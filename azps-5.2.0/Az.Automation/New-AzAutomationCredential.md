---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a0b23cc5e16a723364d234eb2ee9723f291ee5e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285315"
---
# <span data-ttu-id="5349f-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5349f-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="5349f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5349f-102">SYNOPSIS</span></span>
<span data-ttu-id="5349f-103">建立自動化認證。</span><span class="sxs-lookup"><span data-stu-id="5349f-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="5349f-104">句法</span><span class="sxs-lookup"><span data-stu-id="5349f-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5349f-105">說明</span><span class="sxs-lookup"><span data-stu-id="5349f-105">DESCRIPTION</span></span>
<span data-ttu-id="5349f-106">**新的-AzAutomationCredential** Cmdlet 會在 Azure 自動化中建立一個作為 **PSCredential** 物件的認證。</span><span class="sxs-lookup"><span data-stu-id="5349f-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="5349f-107">示例</span><span class="sxs-lookup"><span data-stu-id="5349f-107">EXAMPLES</span></span>

### <span data-ttu-id="5349f-108">範例1：建立認證</span><span class="sxs-lookup"><span data-stu-id="5349f-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5349f-109">第一個命令會將使用者名稱指派給 $User 變數。</span><span class="sxs-lookup"><span data-stu-id="5349f-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="5349f-110">第二個命令會使用 ConvertTo-SecureString Cmdlet，將純文字密碼轉換為安全字串。</span><span class="sxs-lookup"><span data-stu-id="5349f-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="5349f-111">該命令會將該物件儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="5349f-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="5349f-112">第三個命令會根據 $User 和 $Password 建立認證，然後將其儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="5349f-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="5349f-113">最後一個命令會建立一個名為 ContosoCredential 的自動化認證，該認證使用 $Credential。</span><span class="sxs-lookup"><span data-stu-id="5349f-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="5349f-114">參數</span><span class="sxs-lookup"><span data-stu-id="5349f-114">PARAMETERS</span></span>

### <span data-ttu-id="5349f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5349f-115">-AutomationAccountName</span></span>
<span data-ttu-id="5349f-116">指定此 Cmdlet 儲存認證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5349f-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="5349f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5349f-117">-DefaultProfile</span></span>
<span data-ttu-id="5349f-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5349f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5349f-119">-描述</span><span class="sxs-lookup"><span data-stu-id="5349f-119">-Description</span></span>
<span data-ttu-id="5349f-120">指定認證的描述。</span><span class="sxs-lookup"><span data-stu-id="5349f-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="5349f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="5349f-121">-Name</span></span>
<span data-ttu-id="5349f-122">指定認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="5349f-122">Specifies a name for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5349f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5349f-123">-ResourceGroupName</span></span>
<span data-ttu-id="5349f-124">指定此 Cmdlet 建立認證之資源群組的描述。</span><span class="sxs-lookup"><span data-stu-id="5349f-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="5349f-125">-值</span><span class="sxs-lookup"><span data-stu-id="5349f-125">-Value</span></span>
<span data-ttu-id="5349f-126">將認證指定為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="5349f-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5349f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5349f-127">CommonParameters</span></span>
<span data-ttu-id="5349f-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5349f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5349f-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5349f-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5349f-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5349f-130">INPUTS</span></span>

### <span data-ttu-id="5349f-131">System.object</span><span class="sxs-lookup"><span data-stu-id="5349f-131">System.String</span></span>

### <span data-ttu-id="5349f-132">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="5349f-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="5349f-133">輸出</span><span class="sxs-lookup"><span data-stu-id="5349f-133">OUTPUTS</span></span>

### <span data-ttu-id="5349f-134">CredentialInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5349f-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="5349f-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5349f-135">NOTES</span></span>

## <span data-ttu-id="5349f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="5349f-136">RELATED LINKS</span></span>

[<span data-ttu-id="5349f-137">AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5349f-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="5349f-138">移除-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5349f-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="5349f-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5349f-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


