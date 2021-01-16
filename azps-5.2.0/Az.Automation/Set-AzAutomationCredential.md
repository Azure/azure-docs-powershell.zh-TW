---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: e44b9a5c497aba5533d53acdc9aab31cb5ece703
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285188"
---
# <span data-ttu-id="04459-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="04459-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="04459-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04459-102">SYNOPSIS</span></span>
<span data-ttu-id="04459-103">修改自動化認證。</span><span class="sxs-lookup"><span data-stu-id="04459-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="04459-104">句法</span><span class="sxs-lookup"><span data-stu-id="04459-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04459-105">說明</span><span class="sxs-lookup"><span data-stu-id="04459-105">DESCRIPTION</span></span>
<span data-ttu-id="04459-106">**AzAutomationCredential** Cmdlet 會將認證修改成 Azure 自動化中的 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="04459-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="04459-107">示例</span><span class="sxs-lookup"><span data-stu-id="04459-107">EXAMPLES</span></span>

### <span data-ttu-id="04459-108">範例1：更新認證</span><span class="sxs-lookup"><span data-stu-id="04459-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="04459-109">第一個命令會將使用者名稱指派給 $User 變數。</span><span class="sxs-lookup"><span data-stu-id="04459-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="04459-110">第二個命令會使用 ConvertTo-SecureString Cmdlet，將純文字密碼轉換為安全字串。</span><span class="sxs-lookup"><span data-stu-id="04459-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="04459-111">該命令會將該物件儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="04459-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="04459-112">第三個命令會根據 $User 和 $Password 建立認證，然後將其儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="04459-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="04459-113">最後一個命令會修改名為 ContosoCredential 的自動化認證，以在 $Credential 中使用認證。</span><span class="sxs-lookup"><span data-stu-id="04459-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="04459-114">參數</span><span class="sxs-lookup"><span data-stu-id="04459-114">PARAMETERS</span></span>

### <span data-ttu-id="04459-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="04459-115">-AutomationAccountName</span></span>
<span data-ttu-id="04459-116">指定此 Cmdlet 修改認證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="04459-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="04459-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04459-117">-DefaultProfile</span></span>
<span data-ttu-id="04459-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="04459-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04459-119">-描述</span><span class="sxs-lookup"><span data-stu-id="04459-119">-Description</span></span>
<span data-ttu-id="04459-120">指定此 Cmdlet 所修改之認證的描述。</span><span class="sxs-lookup"><span data-stu-id="04459-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="04459-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="04459-121">-Name</span></span>
<span data-ttu-id="04459-122">指定此 Cmdlet 所修改之認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="04459-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="04459-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04459-123">-ResourceGroupName</span></span>
<span data-ttu-id="04459-124">指定此 Cmdlet 修改認證之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="04459-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="04459-125">-值</span><span class="sxs-lookup"><span data-stu-id="04459-125">-Value</span></span>
<span data-ttu-id="04459-126">將認證指定為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="04459-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04459-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04459-127">CommonParameters</span></span>
<span data-ttu-id="04459-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04459-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04459-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="04459-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04459-130">輸入</span><span class="sxs-lookup"><span data-stu-id="04459-130">INPUTS</span></span>

### <span data-ttu-id="04459-131">System.object</span><span class="sxs-lookup"><span data-stu-id="04459-131">System.String</span></span>

### <span data-ttu-id="04459-132">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="04459-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="04459-133">輸出</span><span class="sxs-lookup"><span data-stu-id="04459-133">OUTPUTS</span></span>

### <span data-ttu-id="04459-134">CredentialInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="04459-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="04459-135">筆記</span><span class="sxs-lookup"><span data-stu-id="04459-135">NOTES</span></span>

## <span data-ttu-id="04459-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="04459-136">RELATED LINKS</span></span>

[<span data-ttu-id="04459-137">AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="04459-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="04459-138">新-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="04459-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="04459-139">移除-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="04459-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


