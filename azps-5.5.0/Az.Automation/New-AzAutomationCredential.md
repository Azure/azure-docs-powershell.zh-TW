---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a0b23cc5e16a723364d234eb2ee9723f291ee5e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139551"
---
# <span data-ttu-id="fc03a-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="fc03a-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="fc03a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc03a-102">SYNOPSIS</span></span>
<span data-ttu-id="fc03a-103">建立自動化認證。</span><span class="sxs-lookup"><span data-stu-id="fc03a-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="fc03a-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc03a-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc03a-105">說明</span><span class="sxs-lookup"><span data-stu-id="fc03a-105">DESCRIPTION</span></span>
<span data-ttu-id="fc03a-106">**新的-AzAutomationCredential** Cmdlet 會在 Azure 自動化中建立一個作為 **PSCredential** 物件的認證。</span><span class="sxs-lookup"><span data-stu-id="fc03a-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="fc03a-107">示例</span><span class="sxs-lookup"><span data-stu-id="fc03a-107">EXAMPLES</span></span>

### <span data-ttu-id="fc03a-108">範例1：建立認證</span><span class="sxs-lookup"><span data-stu-id="fc03a-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fc03a-109">第一個命令會將使用者名稱指派給 $User 變數。</span><span class="sxs-lookup"><span data-stu-id="fc03a-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="fc03a-110">第二個命令會使用 ConvertTo-SecureString Cmdlet，將純文字密碼轉換為安全字串。</span><span class="sxs-lookup"><span data-stu-id="fc03a-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="fc03a-111">該命令會將該物件儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="fc03a-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="fc03a-112">第三個命令會根據 $User 和 $Password 建立認證，然後將其儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="fc03a-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="fc03a-113">最後一個命令會建立一個名為 ContosoCredential 的自動化認證，該認證使用 $Credential。</span><span class="sxs-lookup"><span data-stu-id="fc03a-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="fc03a-114">參數</span><span class="sxs-lookup"><span data-stu-id="fc03a-114">PARAMETERS</span></span>

### <span data-ttu-id="fc03a-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fc03a-115">-AutomationAccountName</span></span>
<span data-ttu-id="fc03a-116">指定此 Cmdlet 儲存認證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fc03a-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="fc03a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc03a-117">-DefaultProfile</span></span>
<span data-ttu-id="fc03a-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fc03a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc03a-119">-描述</span><span class="sxs-lookup"><span data-stu-id="fc03a-119">-Description</span></span>
<span data-ttu-id="fc03a-120">指定認證的描述。</span><span class="sxs-lookup"><span data-stu-id="fc03a-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="fc03a-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc03a-121">-Name</span></span>
<span data-ttu-id="fc03a-122">指定認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc03a-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="fc03a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc03a-123">-ResourceGroupName</span></span>
<span data-ttu-id="fc03a-124">指定此 Cmdlet 建立認證之資源群組的描述。</span><span class="sxs-lookup"><span data-stu-id="fc03a-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="fc03a-125">-值</span><span class="sxs-lookup"><span data-stu-id="fc03a-125">-Value</span></span>
<span data-ttu-id="fc03a-126">將認證指定為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="fc03a-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="fc03a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc03a-127">CommonParameters</span></span>
<span data-ttu-id="fc03a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc03a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc03a-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc03a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc03a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="fc03a-130">INPUTS</span></span>

### <span data-ttu-id="fc03a-131">System.object</span><span class="sxs-lookup"><span data-stu-id="fc03a-131">System.String</span></span>

### <span data-ttu-id="fc03a-132">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="fc03a-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="fc03a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="fc03a-133">OUTPUTS</span></span>

### <span data-ttu-id="fc03a-134">CredentialInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="fc03a-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="fc03a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="fc03a-135">NOTES</span></span>

## <span data-ttu-id="fc03a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc03a-136">RELATED LINKS</span></span>

[<span data-ttu-id="fc03a-137">AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="fc03a-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="fc03a-138">移除-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="fc03a-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="fc03a-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="fc03a-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


