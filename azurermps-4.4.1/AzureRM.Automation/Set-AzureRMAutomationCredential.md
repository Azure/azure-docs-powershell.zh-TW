---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
ms.openlocfilehash: e2a461666edf4f06e78f2bc97f47fcb63ab1c19a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447188"
---
# <span data-ttu-id="87ca6-101">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="87ca6-101">Set-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="87ca6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="87ca6-103">修改自動化認證。</span><span class="sxs-lookup"><span data-stu-id="87ca6-103">Modifies an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87ca6-104">句法</span><span class="sxs-lookup"><span data-stu-id="87ca6-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87ca6-105">說明</span><span class="sxs-lookup"><span data-stu-id="87ca6-105">DESCRIPTION</span></span>
<span data-ttu-id="87ca6-106">**AzureRmAutomationCredential** Cmdlet 會將認證修改成 Azure 自動化中的 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="87ca6-106">The **Set-AzureRmAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="87ca6-107">示例</span><span class="sxs-lookup"><span data-stu-id="87ca6-107">EXAMPLES</span></span>

### <span data-ttu-id="87ca6-108">範例1：更新認證</span><span class="sxs-lookup"><span data-stu-id="87ca6-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="87ca6-109">第一個命令會將使用者名稱指派給 $User 變數。</span><span class="sxs-lookup"><span data-stu-id="87ca6-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="87ca6-110">第二個命令會使用 ConvertTo-SecureString Cmdlet，將純文字密碼轉換為安全字串。</span><span class="sxs-lookup"><span data-stu-id="87ca6-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="87ca6-111">該命令會將該物件儲存在 $Password 變數中。</span><span class="sxs-lookup"><span data-stu-id="87ca6-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="87ca6-112">第三個命令會根據 $User 和 $Password 建立認證，然後將其儲存在 $Credential 變數中。</span><span class="sxs-lookup"><span data-stu-id="87ca6-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="87ca6-113">最後一個命令會修改名為 ContosoCredential 的自動化認證，以在 $Credential 中使用認證。</span><span class="sxs-lookup"><span data-stu-id="87ca6-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="87ca6-114">參數</span><span class="sxs-lookup"><span data-stu-id="87ca6-114">PARAMETERS</span></span>

### <span data-ttu-id="87ca6-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="87ca6-115">-AutomationAccountName</span></span>
<span data-ttu-id="87ca6-116">指定此 Cmdlet 修改認證的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="87ca6-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="87ca6-117">-描述</span><span class="sxs-lookup"><span data-stu-id="87ca6-117">-Description</span></span>
<span data-ttu-id="87ca6-118">指定此 Cmdlet 所修改之認證的描述。</span><span class="sxs-lookup"><span data-stu-id="87ca6-118">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="87ca6-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="87ca6-119">-Name</span></span>
<span data-ttu-id="87ca6-120">指定此 Cmdlet 所修改之認證的名稱。</span><span class="sxs-lookup"><span data-stu-id="87ca6-120">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="87ca6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87ca6-121">-ResourceGroupName</span></span>
<span data-ttu-id="87ca6-122">指定此 Cmdlet 修改認證之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="87ca6-122">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="87ca6-123">-值</span><span class="sxs-lookup"><span data-stu-id="87ca6-123">-Value</span></span>
<span data-ttu-id="87ca6-124">將認證指定為 **PSCredential** 物件。</span><span class="sxs-lookup"><span data-stu-id="87ca6-124">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="87ca6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ca6-125">-DefaultProfile</span></span>
<span data-ttu-id="87ca6-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87ca6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ca6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ca6-127">CommonParameters</span></span>
<span data-ttu-id="87ca6-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87ca6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ca6-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="87ca6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ca6-130">輸入</span><span class="sxs-lookup"><span data-stu-id="87ca6-130">INPUTS</span></span>

## <span data-ttu-id="87ca6-131">輸出</span><span class="sxs-lookup"><span data-stu-id="87ca6-131">OUTPUTS</span></span>

### <span data-ttu-id="87ca6-132">CredentialInfo 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="87ca6-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="87ca6-133">筆記</span><span class="sxs-lookup"><span data-stu-id="87ca6-133">NOTES</span></span>

## <span data-ttu-id="87ca6-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="87ca6-134">RELATED LINKS</span></span>

[<span data-ttu-id="87ca6-135">AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="87ca6-135">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="87ca6-136">新-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="87ca6-136">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="87ca6-137">移除-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="87ca6-137">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)


